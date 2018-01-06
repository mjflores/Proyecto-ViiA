# Proyecto-ViiA

//Generar Documento
            Document document = new Document();
            //Definimos la ruta
            PdfWriter.GetInstance(document, new FileStream("C:/Users/FaleTala/Desktop/Hola.pdf", FileMode.Create));
            //Abrir el Documento
            document.Open();
            //Agregar paragraph con el texto Hola Mundo
            document.Add(new Paragraph("Hola Mundo!"));
            document.Add(new Paragraph("\nHola Mundo!"));
            
            //agregando una imagen
            iTextSharp.text.Image imagen = iTextSharp.text.Image.GetInstance("C:/Users/FaleTala/Pictures/Challenge.jpg");
            imagen.BorderWidth = 0;
            imagen.Alignment = Element.ALIGN_LEFT;
            float percentage = 0.0f;
            percentage = 150 / imagen.Width;
            imagen.ScalePercent(percentage * 100);

            //insertamos la imagen
            document.Add(imagen);

            //cerrar Documento
            document.Close();

            //Abrir el documento desde su ruta
System.Diagnostics.Process.Start("C:/Users/FaleTala/Desktop/Hola.pdf");
