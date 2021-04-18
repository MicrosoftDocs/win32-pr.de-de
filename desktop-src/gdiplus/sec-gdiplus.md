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
# <a name="security-considerations-gdi"></a><span data-ttu-id="0da87-103">Sicherheitsüberlegungen: GDI+</span><span class="sxs-lookup"><span data-stu-id="0da87-103">Security Considerations: GDI+</span></span>

<span data-ttu-id="0da87-104">Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit der Programmierung mit Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="0da87-104">This topic provides information about security considerations related to programming with Windows GDI+.</span></span> <span data-ttu-id="0da87-105">Dieses Thema bietet Ihnen nicht alles, was Sie über Sicherheitsprobleme wissen müssen – sondern als Ausgangspunkt und Verweis für diesen Technologiebereich.</span><span class="sxs-lookup"><span data-stu-id="0da87-105">This topic doesn't provide all you need to know about security issues—instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="0da87-106">Überprüfen des Erfolgs von Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="0da87-106">Verifying the Success of Constructors</span></span>](#verifying-the-success-of-constructors)
-   [<span data-ttu-id="0da87-107">Puffer werden zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="0da87-107">Allocating Buffers</span></span>](#allocating-buffers)
-   [<span data-ttu-id="0da87-108">Fehlerüberprüfung</span><span class="sxs-lookup"><span data-stu-id="0da87-108">Error Checking</span></span>](#error-checking)
-   [<span data-ttu-id="0da87-109">Threadsynchronisierung</span><span class="sxs-lookup"><span data-stu-id="0da87-109">Thread Synchronization</span></span>](#thread-synchronization)
-   [<span data-ttu-id="0da87-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0da87-110">Related topics</span></span>](#related-topics)

## <a name="verifying-the-success-of-constructors"></a><span data-ttu-id="0da87-111">Überprüfen des Erfolgs von Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="0da87-111">Verifying the Success of Constructors</span></span>

<span data-ttu-id="0da87-112">Viele der GDI+-Klassen stellen eine [**Image:: getlaststatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) -Methode bereit, die Sie aufrufen können, um zu bestimmen, ob Methoden, die für ein Objekt aufgerufen werden, erfolgreich sind.</span><span class="sxs-lookup"><span data-stu-id="0da87-112">Many of the GDI+ classes provide a [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method that you can call to determine whether methods invoked on an object are successful.</span></span> <span data-ttu-id="0da87-113">Sie können auch **Image:: getlaststatus** aufrufen, um zu bestimmen, ob ein Konstruktor erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="0da87-113">You can also call **Image::GetLastStatus** to determine whether a constructor is successful.</span></span>

<span data-ttu-id="0da87-114">Im folgenden Beispiel wird gezeigt, wie ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt erstellt und die [**Image:: getlaststatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) -Methode aufgerufen wird, um zu bestimmen, ob der Konstruktor erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0da87-114">The following example shows how to construct an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and call the [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method to determine whether the constructor was successful.</span></span> <span data-ttu-id="0da87-115">Die Werte **OK** und **invalidparameter** sind Elemente der [**statusenumeration**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) .</span><span class="sxs-lookup"><span data-stu-id="0da87-115">The values **Ok** and **InvalidParameter** are elements of the [**Status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) enumeration.</span></span>


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



## <a name="allocating-buffers"></a><span data-ttu-id="0da87-116">Puffer werden zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="0da87-116">Allocating Buffers</span></span>

<span data-ttu-id="0da87-117">Mehrere GDI+-Methoden geben numerische Daten oder Zeichendaten in einem Puffer zurück, der vom Aufrufer zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="0da87-117">Several GDI+ methods return numeric or character data in a buffer that is allocated by the caller.</span></span> <span data-ttu-id="0da87-118">Für jede dieser Methoden gibt es eine Begleit Methode, mit der die Größe des erforderlichen Puffers angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0da87-118">For each of those methods, there is a companion method that gives the size of the required buffer.</span></span> <span data-ttu-id="0da87-119">Beispielsweise gibt die [**GraphicsPath:: getpathpoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) -Methode ein Array von [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) -Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="0da87-119">For example, the [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) method returns an array of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="0da87-120">Vor dem Aufrufen von **GraphicsPath:: getpathpoints** müssen Sie einen Puffer zuordnen, der groß genug ist, um das Array zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0da87-120">Before you call **GraphicsPath::GetPathPoints**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="0da87-121">Sie können die Größe des erforderlichen Puffers ermitteln, indem Sie die [**GraphicsPath:: getpointcount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) -Methode eines [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0da87-121">You can determine the size of the required buffer by calling the [**GraphicsPath::GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) method of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span>

<span data-ttu-id="0da87-122">Im folgenden Beispiel wird gezeigt, wie Sie die Anzahl der Punkte in einem [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) -Objekt ermitteln, einen Puffer zuordnen, der so groß genug ist, dass viele Punkte enthalten sind, und anschließend [**GraphicsPath:: getpathpoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) aufrufen, um den Puffer zu füllen.</span><span class="sxs-lookup"><span data-stu-id="0da87-122">The following example shows how to determine the number of points in a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object, allocate a buffer large enough to hold that many points, and then call [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) to fill the buffer.</span></span> <span data-ttu-id="0da87-123">Bevor der Code **GraphicsPath:: getpathpoints** aufruft, überprüft er, ob die Puffer Zuordnung erfolgreich war, indem er sicherstellt, dass der Puffer Zeiger nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="0da87-123">Before the code calls **GraphicsPath::GetPathPoints**, it verifies that the buffer allocation was successful by making sure that the buffer pointer is not **NULL**.</span></span>


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



<span data-ttu-id="0da87-124">Im vorherigen Beispiel wird der neue-Operator verwendet, um einen Puffer zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="0da87-124">The previous example uses the new operator to allocate a buffer.</span></span> <span data-ttu-id="0da87-125">Der New-Operator war praktisch, da der Puffer mit einer bekannten Anzahl von [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) -Objekten aufgefüllt wurde.</span><span class="sxs-lookup"><span data-stu-id="0da87-125">The new operator was convenient because the buffer was filled with a known number of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="0da87-126">In einigen Fällen schreibt GDI+ mehr in den Puffer als ein Array von GDI+-Objekten.</span><span class="sxs-lookup"><span data-stu-id="0da87-126">In some cases, GDI+ writes more into buffer than an array of GDI+ objects.</span></span> <span data-ttu-id="0da87-127">Manchmal wird ein Puffer mit einem Array von GDI+-Objekten zusammen mit zusätzlichen Daten gefüllt, auf die von Membern dieser Objekte verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0da87-127">Sometimes a buffer is filled with an array of GDI+ objects along with additional data that is pointed to by members of those objects.</span></span> <span data-ttu-id="0da87-128">Beispielsweise gibt die [**Image:: getallpropertyitems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) -Methode ein Array von [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) -Objekten zurück, eines für jedes Eigenschafts Element (Metadaten), das im Bild gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="0da87-128">For example, the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method returns an array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects, one for each property item (piece of metadata) stored in the image.</span></span> <span data-ttu-id="0da87-129">**Image:: getallpropertyitems** gibt jedoch mehr als nur das Array von **PropertyItem** -Objekten zurück. Das Array wird mit zusätzlichen Daten angehängt.</span><span class="sxs-lookup"><span data-stu-id="0da87-129">But **Image::GetAllPropertyItems** returns more than just the array of **PropertyItem** objects; it appends the array with additional data.</span></span>

<span data-ttu-id="0da87-130">Vor dem Aufrufen von [**Image:: getallpropertyitems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems)müssen Sie einen Puffer zuordnen, der groß genug ist, um das Array der [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) -Objekte zusammen mit den zusätzlichen Daten aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="0da87-130">Before you call [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), you must allocate a buffer large enough to hold the array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects along with the additional data.</span></span> <span data-ttu-id="0da87-131">Sie können die Methode [**Image:: getpropertysize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) eines Bildobjekts aufrufen, um die Gesamtgröße des erforderlichen Puffers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="0da87-131">You can call the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method of an Image object to determine the total size of the required buffer.</span></span>

<span data-ttu-id="0da87-132">Im folgenden Beispiel wird gezeigt, wie ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt erstellt und später die [**Image:: getallpropertyitems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) -Methode dieses **Bild** Objekts aufgerufen wird, um alle im Bild gespeicherten Eigenschaften Elemente (Metadaten) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0da87-132">The following example shows how to create an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and later call the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method of that **Image** object to retrieve all the property items (metadata) stored in the image.</span></span> <span data-ttu-id="0da87-133">Der Code ordnet einen Puffer auf Grundlage eines Größen Werts zu, der von der [**Image:: getpropertysize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0da87-133">The code allocates a buffer based on a size value returned by the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method.</span></span> <span data-ttu-id="0da87-134">**Image:: getpropertysize** gibt auch einen Count-Wert zurück, der die Anzahl der Eigenschafts Elemente im Bild gibt.</span><span class="sxs-lookup"><span data-stu-id="0da87-134">**Image::GetPropertySize** also returns a count value that gives the number of property items in the image.</span></span> <span data-ttu-id="0da87-135">Beachten Sie, dass der Code die Puffergröße nicht als berechnet `count*sizeof(PropertyItem)` .</span><span class="sxs-lookup"><span data-stu-id="0da87-135">Notice that the code does not calculate the buffer size as `count*sizeof(PropertyItem)`.</span></span> <span data-ttu-id="0da87-136">Ein auf diese Weise berechneter Puffer wäre zu klein.</span><span class="sxs-lookup"><span data-stu-id="0da87-136">A buffer calculated that way would be too small.</span></span>


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



## <a name="error-checking"></a><span data-ttu-id="0da87-137">Fehlerüberprüfung</span><span class="sxs-lookup"><span data-stu-id="0da87-137">Error Checking</span></span>

<span data-ttu-id="0da87-138">Die meisten Codebeispiele in der GDI+-Dokumentation zeigen keine Fehlerüberprüfung an.</span><span class="sxs-lookup"><span data-stu-id="0da87-138">Most of the code examples in the GDI+ documentation do not show error checking.</span></span> <span data-ttu-id="0da87-139">Wenn Sie die Fehlerüberprüfung vervollständigen, wird ein Codebeispiel deutlich länger, und der im Beispiel dargestellte Punkt kann verdecken.</span><span class="sxs-lookup"><span data-stu-id="0da87-139">Complete error checking makes a code example much longer and can obscure the point being illustrated by the example.</span></span> <span data-ttu-id="0da87-140">Sie sollten keine Beispiele aus der Dokumentation direkt in den Produktionscode einfügen. Stattdessen sollten Sie die Beispiele verbessern, indem Sie eine eigene Fehlerüberprüfung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0da87-140">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

<span data-ttu-id="0da87-141">Das folgende Beispiel zeigt eine Möglichkeit zum Implementieren der Fehlerüberprüfung mit GDI+.</span><span class="sxs-lookup"><span data-stu-id="0da87-141">The following example shows one way of implementing error checking with GDI+.</span></span> <span data-ttu-id="0da87-142">Jedes Mal, wenn ein GDI+-Objekt erstellt wird, überprüft der Code, ob der Konstruktor erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0da87-142">Each time a GDI+ object is constructed, the code checks to see whether the constructor was successful.</span></span> <span data-ttu-id="0da87-143">Diese Überprüfung ist besonders wichtig für den [**imagekonstruktor**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , der sich auf das Lesen einer Datei stützt.</span><span class="sxs-lookup"><span data-stu-id="0da87-143">That check is especially important for the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) constructor, which relies on reading a file.</span></span> <span data-ttu-id="0da87-144">Wenn alle vier GDI+-Objekte ([**Grafiken**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image** und [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) erfolgreich erstellt werden, ruft der Code Methoden für diese Objekte auf.</span><span class="sxs-lookup"><span data-stu-id="0da87-144">If all four of the GDI+ objects ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image**, and [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) are constructed successfully, the code calls methods on those objects.</span></span> <span data-ttu-id="0da87-145">Jeder Methodenaufruf wird auf Erfolg geprüft, und im Fall eines Fehlers werden die verbleibenden Methodenaufrufe übersprungen.</span><span class="sxs-lookup"><span data-stu-id="0da87-145">Each method call is checked for success, and in the event of failure, the remaining method calls are skipped.</span></span>


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



## <a name="thread-synchronization"></a><span data-ttu-id="0da87-146">Threadsynchronisierung</span><span class="sxs-lookup"><span data-stu-id="0da87-146">Thread Synchronization</span></span>

<span data-ttu-id="0da87-147">Es ist möglich, dass mehrere Threads auf ein einzelnes GDI+-Objekt zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="0da87-147">It is possible for more than one thread to have access to a single GDI+ object.</span></span> <span data-ttu-id="0da87-148">GDI+ bietet jedoch keinen automatischen Synchronisierungs Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="0da87-148">However, GDI+ does not provide any automatic synchronization mechanism.</span></span> <span data-ttu-id="0da87-149">Wenn also zwei Threads in der Anwendung über einen Zeiger auf dasselbe GDI+-Objekt verfügen, müssen Sie den Zugriff auf dieses Objekt synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="0da87-149">So if two threads in your application have a pointer to the same GDI+ object, it is your responsibility to synchronize access to that object.</span></span>

<span data-ttu-id="0da87-150">Einige GDI+-Methoden geben **ObjectBusy** zurück, wenn ein Thread versucht, eine Methode aufzurufen, während ein anderer Thread eine Methode für das gleiche Objekt ausführt.</span><span class="sxs-lookup"><span data-stu-id="0da87-150">Some GDI+ methods return **ObjectBusy** if a thread attempts to call a method while another thread is executing a method on the same object.</span></span> <span data-ttu-id="0da87-151">Versuchen Sie nicht, den Zugriff auf ein Objekt basierend auf dem Rückgabewert **ObjectBusy** zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="0da87-151">Do not try to synchronize access to an object based on the **ObjectBusy** return value.</span></span> <span data-ttu-id="0da87-152">Verwenden Sie stattdessen jedes Mal, wenn Sie auf ein Element zugreifen oder eine Methode des Objekts aufrufen, den Aufruf innerhalb eines kritischen Abschnitts, oder verwenden Sie ein anderes Standardverfahren für die Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="0da87-152">Instead, each time you access a member or call a method of the object, place the call inside a critical section, or use some other standard synchronization technique.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0da87-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0da87-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0da87-154">MSDN Security Developer Center</span><span class="sxs-lookup"><span data-stu-id="0da87-154">MSDN Security Developer Center</span></span>](https://msdn.microsoft.com/security/)
</dt> <dt>

<span data-ttu-id="0da87-155">[Sicherheits How-To Ressourcen](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="0da87-155">[Security How-To Resources](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span></span>
</dt> <dt>

[<span data-ttu-id="0da87-156">TechNet-Security Center</span><span class="sxs-lookup"><span data-stu-id="0da87-156">TechNet Security Center</span></span>](https://technet.microsoft.com/security/)
</dt> </dl>

 

 
