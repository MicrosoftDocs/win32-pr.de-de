---
description: Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit der Programmierung mit Windows GDI+.
ms.assetid: 411e16e4-ad8f-4567-8964-564f08283ba5
title: 'Sicherheitsüberlegungen: GDI+'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc741911af403f079d16b4759431eaaa4b6cf55d5dad11826768033036aef75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035998"
---
# <a name="security-considerations-gdi"></a>Sicherheitsüberlegungen: GDI+

Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit der Programmierung mit Windows GDI+. Dieses Thema enthält nicht alles, was Sie über Sicherheitsprobleme wissen müssen. Verwenden Sie es stattdessen als Ausgangspunkt und Referenz für diesen Technologiebereich.

-   [Überprüfen des Erfolgs von Konstruktoren](#verifying-the-success-of-constructors)
-   [Zuordnen von Puffern](#allocating-buffers)
-   [Fehlerüberprüfung](#error-checking)
-   [Threadsynchronisierung](#thread-synchronization)
-   [Zugehörige Themen](#related-topics)

## <a name="verifying-the-success-of-constructors"></a>Überprüfen des Erfolgs von Konstruktoren

Viele der GDI+ stellen eine [**Image::GetLastStatus-Methode**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) bereit, die Sie aufrufen können, um zu bestimmen, ob für ein Objekt aufgerufene Methoden erfolgreich sind. Sie können auch **Image::GetLastStatus aufrufen,** um zu bestimmen, ob ein Konstruktor erfolgreich ist.

Das folgende Beispiel zeigt, wie sie ein [**Image-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) erstellen und die [**Image::GetLastStatus-Methode**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) aufrufen, um zu bestimmen, ob der Konstruktor erfolgreich war. Die Werte **OK** und **InvalidParameter** sind Elemente der [**Status-Enumeration.**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status)


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



## <a name="allocating-buffers"></a>Zuordnen von Puffern

Mehrere GDI+ methoden geben numerische oder Zeichendaten in einem Puffer zurück, der vom Aufrufer zugeordnet wird. Für jede dieser Methoden gibt es eine Begleitmethode, die die Größe des erforderlichen Puffers angibt. Die [**GraphicsPath::GetPathPoints-Methode**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) gibt beispielsweise ein Array von [**Point-Objekten**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) zurück. Bevor Sie **GraphicsPath::GetPathPoints** aufrufen, müssen Sie einen Puffer zuordnen, der groß genug ist, um dieses Array zu speichern. Sie können die Größe des erforderlichen Puffers ermitteln, indem Sie die [**GraphicsPath::GetPointCount-Methode**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) eines [**GraphicsPath-Objekts**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) aufrufen.

Im folgenden Beispiel wird gezeigt, wie Sie die Anzahl der Punkte in einem [**GraphicsPath-Objekt**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) bestimmen, einen Puffer zuordnen, der groß genug ist, um diese Anzahl von Punkten zu halten, und dann [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) aufrufen, um den Puffer zu füllen. Bevor der Code **GraphicsPath::GetPathPoints** aufruft, wird überprüft, ob die Pufferzuordnung erfolgreich war, indem sichergestellt wird, dass der Pufferzeiger nicht **NULL ist.**


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



Im vorherigen Beispiel wird der new-Operator verwendet, um einen Puffer zu reservieren. Der neue Operator war praktisch, da der Puffer mit einer bekannten Anzahl von [**Point-Objekten gefüllt**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) wurde. In einigen Fällen schreibt GDI+ mehr in den Puffer als ein Array von GDI+ Objekten. Manchmal wird ein Puffer mit einem Array von GDI+-Objekten sowie zusätzlichen Daten gefüllt, auf die member dieser Objekte verweist. Die [**Image::GetAllPropertyItems-Methode**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) gibt beispielsweise ein Array von [**PropertyItem-Objekten**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) zurück, eines für jedes Eigenschaftenelement (Metadatenelement), das im Bild gespeichert ist. **Image::GetAllPropertyItems gibt** jedoch mehr als nur das Array von **PropertyItem-Objekten** zurück. Es fügt das Array mit zusätzlichen Daten an.

Bevor Sie [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems)aufrufen, müssen Sie einen Puffer zuordnen, der groß genug ist, um das Array von [**PropertyItem-Objekten**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) zusammen mit den zusätzlichen Daten zu speichern. Sie können die [**Image::GetPropertySize-Methode**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) eines Image-Objekts aufrufen, um die Gesamtgröße des erforderlichen Puffers zu bestimmen.

Das folgende Beispiel zeigt, wie Sie ein [**Image-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) erstellen und später die [**Image::GetAllPropertyItems-Methode**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) dieses **Image-Objekts** aufrufen, um alle im Bild gespeicherten Eigenschaftenelemente (Metadaten) abzurufen. Der Code ordnet einen Puffer basierend auf einem Größenwert zu, der von der [**Image::GetPropertySize-Methode zurückgegeben**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) wird. **Image::GetPropertySize gibt** auch einen Count-Wert zurück, der die Anzahl der Eigenschaftselemente im Bild angibt. Beachten Sie, dass der Code die Puffergröße nicht als `count*sizeof(PropertyItem)` berechnet. Ein auf diese Weise berechneter Puffer wäre zu klein.


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

Die meisten Codebeispiele in der GDI+ zeigen keine Fehlerüberprüfung. Die vollständige Fehlerüberprüfung macht ein Codebeispiel viel länger und kann den Punkt, der im Beispiel veranschaulicht wird, verdecken. Sie sollten Beispiele aus der Dokumentation nicht direkt in Produktionscode einfügen. Stattdessen sollten Sie die Beispiele verbessern, indem Sie Eine eigene Fehlerüberprüfung hinzufügen.

Das folgende Beispiel zeigt eine Möglichkeit zum Implementieren der Fehlerüberprüfung mit GDI+. Jedes Mal, wenn GDI+ erstellt wird, überprüft der Code, ob der Konstruktor erfolgreich war. Diese Überprüfung ist besonders wichtig für den [**Image-Konstruktor,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) der auf dem Lesen einer Datei basiert. Wenn alle vier GDI+ Objekte ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image** und [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) erfolgreich erstellt wurden, ruft der Code Methoden für diese Objekte auf. Jeder Methodenaufruf wird auf Erfolg überprüft, und im Falle eines Fehlers werden die verbleibenden Methodenaufrufe übersprungen.


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

Es ist möglich, dass mehrere Threads Zugriff auf ein einzelnes GDI+ haben. Allerdings bietet GDI+ keinen automatischen Synchronisierungsmechanismus. Wenn also zwei Threads in Ihrer Anwendung einen Zeiger auf dasselbe GDI+-Objekt haben, liegt es in Ihrer Verantwortung, den Zugriff auf dieses Objekt zu synchronisieren.

Einige GDI+-Methoden geben **ObjectBusy** zurück, wenn ein Thread versucht, eine Methode auf aufruft, während ein anderer Thread eine Methode für dasselbe Objekt ausgeführt. Versuchen Sie nicht, den Zugriff auf ein Objekt basierend auf dem **ObjectBusy-Rückgabewert** zu synchronisieren. Platzieren Sie stattdessen jedes Mal, wenn Sie auf einen Member zugreifen oder eine Methode des Objekts aufrufen, den Aufruf in einem kritischen Abschnitt, oder verwenden Sie eine andere Standardsynchronisierungstechnik.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MSDN Security Developer Center](https://msdn.microsoft.com/security/)
</dt> <dt>

[SicherheitsHow-To Ressourcen](/previous-versions/msp-n-p/ff650055(v=pandp.10))
</dt> <dt>

[TechNet Security Center](https://technet.microsoft.com/security/)
</dt> </dl>

 

 
