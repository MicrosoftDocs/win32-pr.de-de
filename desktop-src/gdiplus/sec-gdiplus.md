---
description: Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit der Programmierung mit Windows GDI+.
ms.assetid: 411e16e4-ad8f-4567-8964-564f08283ba5
title: 'Sicherheitsüberlegungen: GDI+'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d8c9d50393708e58651566ee90adcb4339cb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994166"
---
# <a name="security-considerations-gdi"></a>Sicherheitsüberlegungen: GDI+

Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit der Programmierung mit Windows GDI+. Dieses Thema bietet Ihnen nicht alles, was Sie über Sicherheitsprobleme wissen müssen – sondern als Ausgangspunkt und Verweis für diesen Technologiebereich.

-   [Überprüfen des Erfolgs von Konstruktoren](#verifying-the-success-of-constructors)
-   [Puffer werden zugewiesen.](#allocating-buffers)
-   [Fehlerüberprüfung](#error-checking)
-   [Threadsynchronisierung](#thread-synchronization)
-   [Zugehörige Themen](#related-topics)

## <a name="verifying-the-success-of-constructors"></a>Überprüfen des Erfolgs von Konstruktoren

Viele der GDI+-Klassen stellen eine [**Image:: getlaststatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) -Methode bereit, die Sie aufrufen können, um zu bestimmen, ob Methoden, die für ein Objekt aufgerufen werden, erfolgreich sind. Sie können auch **Image:: getlaststatus** aufrufen, um zu bestimmen, ob ein Konstruktor erfolgreich ist.

Im folgenden Beispiel wird gezeigt, wie ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt erstellt und die [**Image:: getlaststatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) -Methode aufgerufen wird, um zu bestimmen, ob der Konstruktor erfolgreich war. Die Werte **OK** und **invalidparameter** sind Elemente der [**statusenumeration**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) .


```C++
Image myImage(L"Climber.jpg");
Status st = myImage.GetLastStatus();

if(Ok == st)
   // The constructor was successful. Use myImage.
else if(InvalidParameter == st)
   // The constructor failed because of an invalid parameter.
else
   // Compare st to other elements of the Status 
   // enumeration or do general error processing.
```



## <a name="allocating-buffers"></a>Puffer werden zugewiesen.

Mehrere GDI+-Methoden geben numerische Daten oder Zeichendaten in einem Puffer zurück, der vom Aufrufer zugeordnet wird. Für jede dieser Methoden gibt es eine Begleit Methode, mit der die Größe des erforderlichen Puffers angegeben wird. Beispielsweise gibt die [**GraphicsPath:: getpathpoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) -Methode ein Array von [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) -Objekten zurück. Vor dem Aufrufen von **GraphicsPath:: getpathpoints** müssen Sie einen Puffer zuordnen, der groß genug ist, um das Array zu speichern. Sie können die Größe des erforderlichen Puffers ermitteln, indem Sie die [**GraphicsPath:: getpointcount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) -Methode eines [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekts aufrufen.

Im folgenden Beispiel wird gezeigt, wie Sie die Anzahl der Punkte in einem [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt ermitteln, einen Puffer zuordnen, der so groß genug ist, dass viele Punkte enthalten sind, und anschließend [**GraphicsPath:: getpathpoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) aufrufen, um den Puffer zu füllen. Bevor der Code **GraphicsPath:: getpathpoints** aufruft, überprüft er, ob die Puffer Zuordnung erfolgreich war, indem er sicherstellt, dass der Puffer Zeiger nicht **null** ist.


```C++
GraphicsPath path;
path.AddEllipse(10, 10, 200, 100);

INT count = path.GetPointCount();          // get the size
Point* pointArray = new Point[count];      // allocate the buffer

if(pointArray)  // Check for successful allocation.
{
   path.GetPathPoints(pointArray, count);  // get the data
   ...                                     // use pointArray
   delete[] pointArray;                    // release the buffer
   pointArray = NULL;
}
```



Im vorherigen Beispiel wird der neue-Operator verwendet, um einen Puffer zuzuweisen. Der New-Operator war praktisch, da der Puffer mit einer bekannten Anzahl von [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) -Objekten aufgefüllt wurde. In einigen Fällen schreibt GDI+ mehr in den Puffer als ein Array von GDI+-Objekten. Manchmal wird ein Puffer mit einem Array von GDI+-Objekten zusammen mit zusätzlichen Daten gefüllt, auf die von Membern dieser Objekte verwiesen wird. Beispielsweise gibt die [**Image:: getallpropertyitems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) -Methode ein Array von [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) -Objekten zurück, eines für jedes Eigenschafts Element (Metadaten), das im Bild gespeichert ist. **Image:: getallpropertyitems** gibt jedoch mehr als nur das Array von **PropertyItem** -Objekten zurück. Das Array wird mit zusätzlichen Daten angehängt.

Vor dem Aufrufen von [**Image:: getallpropertyitems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems)müssen Sie einen Puffer zuordnen, der groß genug ist, um das Array der [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) -Objekte zusammen mit den zusätzlichen Daten aufzunehmen. Sie können die Methode [**Image:: getpropertysize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) eines Bildobjekts aufrufen, um die Gesamtgröße des erforderlichen Puffers zu bestimmen.

Im folgenden Beispiel wird gezeigt, wie ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt erstellt und später die [**Image:: getallpropertyitems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) -Methode dieses **Bild** Objekts aufgerufen wird, um alle im Bild gespeicherten Eigenschaften Elemente (Metadaten) abzurufen. Der Code ordnet einen Puffer auf Grundlage eines Größen Werts zu, der von der [**Image:: getpropertysize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) -Methode zurückgegeben wird. **Image:: getpropertysize** gibt auch einen Count-Wert zurück, der die Anzahl der Eigenschafts Elemente im Bild gibt. Beachten Sie, dass der Code die Puffergröße nicht als berechnet `count*sizeof(PropertyItem)` . Ein auf diese Weise berechneter Puffer wäre zu klein.


```C++
UINT count = 0;
UINT size = 0;
Image myImage(L"FakePhoto.jpg");
myImage.GetPropertySize(&size, &count);

// GetAllPropertyItems returns an array of PropertyItem objects
// along with additional data. Allocate a buffer large enough to 
// receive the array and the additional data.
PropertyItem* propBuffer =(PropertyItem*)malloc(size);

if(propBuffer)
{
   myImage.GetAllPropertyItems(size, count, propBuffer);
   ...
   free(propBuffer);
   propBuffer = NULL;
}
```



## <a name="error-checking"></a>Fehlerüberprüfung

Die meisten Codebeispiele in der GDI+-Dokumentation zeigen keine Fehlerüberprüfung an. Wenn Sie die Fehlerüberprüfung vervollständigen, wird ein Codebeispiel deutlich länger, und der im Beispiel dargestellte Punkt kann verdecken. Sie sollten keine Beispiele aus der Dokumentation direkt in den Produktionscode einfügen. Stattdessen sollten Sie die Beispiele verbessern, indem Sie eine eigene Fehlerüberprüfung hinzufügen.

Das folgende Beispiel zeigt eine Möglichkeit zum Implementieren der Fehlerüberprüfung mit GDI+. Jedes Mal, wenn ein GDI+-Objekt erstellt wird, überprüft der Code, ob der Konstruktor erfolgreich war. Diese Überprüfung ist besonders wichtig für den [**imagekonstruktor**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , der sich auf das Lesen einer Datei stützt. Wenn alle vier GDI+-Objekte ([**Grafiken**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image** und [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) erfolgreich erstellt werden, ruft der Code Methoden für diese Objekte auf. Jeder Methodenaufruf wird auf Erfolg geprüft, und im Fall eines Fehlers werden die verbleibenden Methodenaufrufe übersprungen.


```C++
Status GdipExample(HDC hdc)
{
   Status status = GenericError;
   INT count = 0;
   Point* points = NULL;

   Graphics graphics(hdc);
   status = graphics.GetLastStatus();
   if(Ok != status)
      return status;

   GraphicsPath path;
   status = path.GetLastStatus();
   if(Ok != status)
      return status;

   Image image(L"MyTexture.bmp");
   status = image.GetLastStatus();
   if(Ok != status)
      return status;

   TextureBrush brush(&image);
   status = brush.GetLastStatus();
   if(Ok != status)
      return status;

   status = path.AddEllipse(10, 10, 200, 100);

   if(Ok == status)
   {
      status = path.AddBezier(40, 130, 200, 130, 200, 200, 60, 200);
   }
  
   if(Ok == status)
   {
      count = path.GetPointCount();
      status = path.GetLastStatus();
   }

   if(Ok == status)
   {
      points = new Point[count];

      if(NULL == points)
         status = OutOfMemory;
   }

   if(Ok == status)
   {
      status = path.GetPathPoints(points, count);  
   }
  
   if(Ok == status)
   {
      status = graphics.FillPath(&brush, &path);
   }
   
   if(Ok == status)
   {
      for(int j = 0; j < count; ++j)
      {
         status = graphics.FillEllipse(
         &brush, points[j].X - 5, points[j].Y - 5, 10, 10);
      }
   }

   if(points)
   {
      delete[] points;
      points = NULL;
   }

   return status;
}
```



## <a name="thread-synchronization"></a>Threadsynchronisierung

Es ist möglich, dass mehrere Threads auf ein einzelnes GDI+-Objekt zugreifen können. GDI+ bietet jedoch keinen automatischen Synchronisierungs Mechanismus. Wenn also zwei Threads in der Anwendung über einen Zeiger auf dasselbe GDI+-Objekt verfügen, müssen Sie den Zugriff auf dieses Objekt synchronisieren.

Einige GDI+-Methoden geben **ObjectBusy** zurück, wenn ein Thread versucht, eine Methode aufzurufen, während ein anderer Thread eine Methode für das gleiche Objekt ausführt. Versuchen Sie nicht, den Zugriff auf ein Objekt basierend auf dem Rückgabewert **ObjectBusy** zu synchronisieren. Verwenden Sie stattdessen jedes Mal, wenn Sie auf ein Element zugreifen oder eine Methode des Objekts aufrufen, den Aufruf innerhalb eines kritischen Abschnitts, oder verwenden Sie ein anderes Standardverfahren für die Synchronisierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MSDN Security Developer Center](https://msdn.microsoft.com/security/)
</dt> <dt>

[Sicherheits How-To Ressourcen](/previous-versions/msp-n-p/ff650055(v=pandp.10))
</dt> <dt>

[TechNet-Security Center](https://technet.microsoft.com/security/)
</dt> </dl>

 

 
