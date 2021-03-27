---
description: Einige Bilddateien enthalten Metadaten, die Sie lesen können, um die Funktionen des Images zu ermitteln.
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: Lesen und Schreiben von Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f599c1134efc8768d0b6ed59deaae8adf9f6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751313"
---
# <a name="reading-and-writing-metadata"></a><span data-ttu-id="669f9-103">Lesen und Schreiben von Metadaten</span><span class="sxs-lookup"><span data-stu-id="669f9-103">Reading and Writing Metadata</span></span>

<span data-ttu-id="669f9-104">Einige Bilddateien enthalten Metadaten, die Sie lesen können, um die Funktionen des Images zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="669f9-104">Some image files contain metadata that you can read to determine features of the image.</span></span> <span data-ttu-id="669f9-105">Beispielsweise kann ein digitales Foto Metadaten enthalten, die Sie lesen können, um die Marke und das Modell der Kamera zu ermitteln, die zum Erfassen des Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="669f9-105">For example, a digital photograph might contain metadata that you can read to determine the make and model of the camera used to capture the image.</span></span> <span data-ttu-id="669f9-106">Mit Windows GDI+ können Sie vorhandene Metadaten lesen, und Sie können auch neue Metadaten in Bilddateien schreiben.</span><span class="sxs-lookup"><span data-stu-id="669f9-106">With Windows GDI+, you can read existing metadata, and you can also write new metadata to image files.</span></span>

<span data-ttu-id="669f9-107">GDI+ bietet eine einheitliche Möglichkeit zum Speichern und Abrufen von Metadaten aus Bilddateien in verschiedenen Formaten.</span><span class="sxs-lookup"><span data-stu-id="669f9-107">GDI+ provides a uniform way of storing and retrieving metadata from image files in various formats.</span></span> <span data-ttu-id="669f9-108">In GDI+ wird ein *Metadatenelement als Eigenschaften Element* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="669f9-108">In GDI+, a piece of metadata is called a *property item*.</span></span> <span data-ttu-id="669f9-109">Sie können Metadaten speichern und abrufen, indem Sie die **SetPropertyItem** -Methode und die **GetPropertyItem** -Methode der [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse aufrufen, und Sie müssen sich nicht um die Details kümmern, wie ein bestimmtes Dateiformat diese Metadaten speichert.</span><span class="sxs-lookup"><span data-stu-id="669f9-109">You can store and retrieve metadata by calling the **SetPropertyItem** and **GetPropertyItem** methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned about the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="669f9-110">GDI+ unterstützt derzeit Metadaten für die Dateiformate TIFF, JPEG, EXIF und PNG.</span><span class="sxs-lookup"><span data-stu-id="669f9-110">GDI+ currently supports metadata for the TIFF, JPEG, Exif, and PNG file formats.</span></span> <span data-ttu-id="669f9-111">Das EXIF-Format, das angibt, wie von digitalen Digitalkameras erfasste Bilder gespeichert werden, basiert auf den TIFF-und JPEG-Formaten.</span><span class="sxs-lookup"><span data-stu-id="669f9-111">The Exif format, which specifies how to store images captured by digital still cameras, is built on top of the TIFF and JPEG formats.</span></span> <span data-ttu-id="669f9-112">EXIF verwendet das TIFF-Format für unkomprimierte Pixeldaten und das JPEG-Format für komprimierte Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="669f9-112">Exif uses the TIFF format for uncompressed pixel data and the JPEG format for compressed pixel data.</span></span>

<span data-ttu-id="669f9-113">GDI+ definiert einen Satz von Eigenschafts Tags, die Eigenschaften Elemente identifizieren.</span><span class="sxs-lookup"><span data-stu-id="669f9-113">GDI+ defines a set of property tags that identify property items.</span></span> <span data-ttu-id="669f9-114">Bestimmte Tags sind universell. Das heißt, Sie werden von allen Dateiformaten unterstützt, die im vorherigen Abschnitt erwähnt wurden.</span><span class="sxs-lookup"><span data-stu-id="669f9-114">Certain tags are general-purpose; that is, they are supported by all of the file formats mentioned in the preceding paragraph.</span></span> <span data-ttu-id="669f9-115">Andere Tags sind besondere Zwecke und gelten nur für bestimmte Formate.</span><span class="sxs-lookup"><span data-stu-id="669f9-115">Other tags are special-purpose and apply only to certain formats.</span></span> <span data-ttu-id="669f9-116">Wenn Sie versuchen, ein Eigenschaften Element in einer Datei zu speichern, die dieses Eigenschaften Element nicht unterstützt, wird die Anforderung von GDI+ ignoriert.</span><span class="sxs-lookup"><span data-stu-id="669f9-116">If you try to save a property item to a file that does not support that property item, GDI+ ignores the request.</span></span> <span data-ttu-id="669f9-117">Genauer gesagt gibt die [**Image:: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) -Methode propertynotsupported zurück.</span><span class="sxs-lookup"><span data-stu-id="669f9-117">More specifically, the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) method returns PropertyNotSupported.</span></span>

<span data-ttu-id="669f9-118">Sie können die Eigenschaften Elemente, die in einer Bilddatei gespeichert sind, durch Aufrufen von " [**Image:: getpropertyidlist**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist)" ermitteln.</span><span class="sxs-lookup"><span data-stu-id="669f9-118">You can determine the property items that are stored in an image file by calling [**Image::GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span></span> <span data-ttu-id="669f9-119">Wenn Sie versuchen, ein Eigenschaften Element abzurufen, das sich nicht in der Datei befindet, wird die Anforderung von GDI+ ignoriert.</span><span class="sxs-lookup"><span data-stu-id="669f9-119">If you try to retrieve a property item that is not in the file, GDI+ ignores the request.</span></span> <span data-ttu-id="669f9-120">Genauer gesagt gibt die [**Image:: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) -Methode propertynotfound zurück.</span><span class="sxs-lookup"><span data-stu-id="669f9-120">More specifically, the [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) method returns PropertyNotFound.</span></span>

## <a name="reading-metadata-from-a-file"></a><span data-ttu-id="669f9-121">Lesen von Metadaten aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="669f9-121">Reading Metadata from a File</span></span>

<span data-ttu-id="669f9-122">Die folgende Konsolenanwendung ruft die **getpropertysize** -Methode eines [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekts auf, um zu bestimmen, wie viele Metadaten in der Datei FakePhoto.jpg sind.</span><span class="sxs-lookup"><span data-stu-id="669f9-122">The following console application calls the **GetPropertySize** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object to determine how many pieces of metadata are in the file FakePhoto.jpg.</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   UINT    size = 0;
   UINT    count = 0;
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n", count);
   printf("The total size of the metadata is %d bytes.\n", size);
 
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="669f9-123">Der vorangehende Code hat zusammen mit einer bestimmten Datei FakePhoto.jpg die folgende Ausgabe erzeugt:</span><span class="sxs-lookup"><span data-stu-id="669f9-123">The preceding code, along with a particular file, FakePhoto.jpg, produced the following output:</span></span>


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



<span data-ttu-id="669f9-124">GDI+ speichert ein einzelnes Metadatenelement in einem [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="669f9-124">GDI+ stores an individual piece of metadata in a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object.</span></span> <span data-ttu-id="669f9-125">Sie können die **getallpropertyitems** -Methode der [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse aufrufen, um alle Metadaten aus einer Datei abzurufen.</span><span class="sxs-lookup"><span data-stu-id="669f9-125">You can call the **GetAllPropertyItems** method of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class to retrieve all the metadata from a file.</span></span> <span data-ttu-id="669f9-126">Die **getallpropertyitems** -Methode gibt ein Array von **PropertyItem** -Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="669f9-126">The **GetAllPropertyItems** method returns an array of **PropertyItem** objects.</span></span> <span data-ttu-id="669f9-127">Vor dem Aufrufen von **getallpropertyitems** müssen Sie einen Puffer zuordnen, der groß genug ist, um das Array zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="669f9-127">Before you call **GetAllPropertyItems**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="669f9-128">Sie können die **getpropertysize** -Methode der **Image** -Klasse aufrufen, um die Größe (in Bytes) des erforderlichen Puffers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="669f9-128">You can call the **GetPropertySize** method of the **Image** class to get the size (in bytes) of the required buffer.</span></span>

<span data-ttu-id="669f9-129">Ein [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) -Objekt verfügt über die folgenden vier öffentlichen Member:</span><span class="sxs-lookup"><span data-stu-id="669f9-129">A [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object has the following four public members:</span></span>



|            |                                                                                                                                                                                                                                                                                                        |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="669f9-130">**id**</span><span class="sxs-lookup"><span data-stu-id="669f9-130">**id**</span></span>     | <span data-ttu-id="669f9-131">Ein-Tag, das das Metadatenelement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="669f9-131">A tag that identifies the metadata item.</span></span> <span data-ttu-id="669f9-132">Die Werte, die **ID** zugewiesen werden können (propertytagimagetitle, propertytagequipmake, propertytagexifexposuretime und like), werden in gdiplusimaging. h definiert.</span><span class="sxs-lookup"><span data-stu-id="669f9-132">The values that can be assigned to **id** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime, and the like) are defined in Gdiplusimaging.h.</span></span>                                                                                           |
| <span data-ttu-id="669f9-133">**length**</span><span class="sxs-lookup"><span data-stu-id="669f9-133">**length**</span></span> | <span data-ttu-id="669f9-134">Die Länge (in Byte) des Arrays von Werten, auf die vom **wertdatenmember** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="669f9-134">The length, in bytes, of the array of values pointed to by the **value** data member.</span></span> <span data-ttu-id="669f9-135">Beachten Sie Folgendes: Wenn das **Typdatenmember** auf propertytagtybäuercii festgelegt ist, ist das length-Datenmember die **Länge** einer null-terminierten Zeichenfolge, einschließlich des NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="669f9-135">Note that if the **type** data member is set to PropertyTagTypeASCII, then the length data member is the **length** of a null-terminated character string, including the NULL terminator.</span></span>                        |
| <span data-ttu-id="669f9-136">**type**</span><span class="sxs-lookup"><span data-stu-id="669f9-136">**type**</span></span>   | <span data-ttu-id="669f9-137">Der Datentyp der Werte im Array, auf die vom wertdatenmember verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="669f9-137">The data type of the values in the array pointed to by the value data member.</span></span> <span data-ttu-id="669f9-138">Konstanten (propertytagtypebyte, propertytagtybäuercii und like), die verschiedene Datentypen darstellen, werden in den [**Tagtyp Konstanten des Image-Eigenschaften**](-gdiplus-constant-image-property-tag-type-constants.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="669f9-138">Constants (PropertyTagTypeByte, PropertyTagTypeASCII, and the like) that represent various data types are described in [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span> |
| <span data-ttu-id="669f9-139">**value**</span><span class="sxs-lookup"><span data-stu-id="669f9-139">**value**</span></span>  | <span data-ttu-id="669f9-140">Ein Zeiger auf ein Array von-Werten.</span><span class="sxs-lookup"><span data-stu-id="669f9-140">A pointer to an array of values.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="669f9-141">Die folgende Konsolenanwendung liest und zeigt die sieben Metadatenelemente in der Datei FakePhoto.jpg an.</span><span class="sxs-lookup"><span data-stu-id="669f9-141">The following console application reads and displays the seven pieces of metadata in the file FakePhoto.jpg.</span></span> <span data-ttu-id="669f9-142">Die Main-Funktion basiert auf der Hilfsfunktion propertytypefromword, die nach der Main-Funktion angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="669f9-142">The main function relies on the helper function PropertyTypeFromWORD, which is shown following the main function.</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <strsafe.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  size = 0;
   UINT  count = 0;

   #define MAX_PROPTYPE_SIZE 30
   WCHAR strPropertyType[MAX_PROPTYPE_SIZE] = L"";

   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");

   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n\n", count);

   // GetAllPropertyItems returns an array of PropertyItem objects.
   // Allocate a buffer large enough to receive that array.
   PropertyItem* pPropBuffer =(PropertyItem*)malloc(size);

   // Get the array of PropertyItem objects.
   bitmap->GetAllPropertyItems(size, count, pPropBuffer);

   // For each PropertyItem in the array, display the id, type, and length.
   for(UINT j = 0; j < count; ++j)
   {
      // Convert the property type from a WORD to a string.
      PropertyTypeFromWORD(
         pPropBuffer[j].type, strPropertyType, MAX_PROPTYPE_SIZE);

      printf("Property Item %d\n", j);
      printf("  id: 0x%x\n", pPropBuffer[j].id);
      wprintf(L"  type: %s\n", strPropertyType);
      printf("  length: %d bytes\n\n", pPropBuffer[j].length);
   }

   free(pPropBuffer);
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
} // main

// Helper function
HRESULT PropertyTypeFromWORD(WORD index, WCHAR* string, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   WCHAR* propertyTypes[] = {
      L"Nothing",                   // 0
      L"PropertyTagTypeByte",       // 1
      L"PropertyTagTypeASCII",      // 2
      L"PropertyTagTypeShort",      // 3
      L"PropertyTagTypeLong",       // 4
      L"PropertyTagTypeRational",   // 5
      L"Nothing",                   // 6
      L"PropertyTagTypeUndefined",  // 7
      L"Nothing",                   // 8
      L"PropertyTagTypeSLONG",      // 9
      L"PropertyTagTypeSRational"}; // 10

   hr = StringCchCopyW(string, maxChars, propertyTypes[index]);
   return hr;
}
```



<span data-ttu-id="669f9-143">Die vorherige Konsolenanwendung erzeugt die folgende Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="669f9-143">The preceding console application produces the following output:</span></span>


```
Property Item 0
  id: 0x320
  type: PropertyTagTypeASCII
  length: 16 bytes
Property Item 1
  id: 0x10f
  type: PropertyTagTypeASCII
  length: 17 bytes
Property Item 2
  id: 0x110
  type: PropertyTagTypeASCII
  length: 7 bytes
Property Item 3
  id: 0x9003
  type: PropertyTagTypeASCII
  length: 20 bytes
Property Item 4
  id: 0x829a
  type: PropertyTagTypeRational
  length: 8 bytes
Property Item 5
  id: 0x5090
  type: PropertyTagTypeShort
  length: 128 bytes
Property Item 6
  id: 0x5091
  type: PropertyTagTypeShort
  length: 128 bytes
```



<span data-ttu-id="669f9-144">Die obige Ausgabe zeigt eine hexadezimale ID-Nummer für jedes Eigenschafts Element an.</span><span class="sxs-lookup"><span data-stu-id="669f9-144">The preceding output shows a hexadecimal ID number for each property item.</span></span> <span data-ttu-id="669f9-145">Sie können diese ID-Nummern in den [tagkonstanten der Abbild Eigenschaften](-gdiplus-constant-image-property-tag-constants.md) nachschlagen und ermitteln, dass Sie die folgenden Eigenschaften Tags darstellen.</span><span class="sxs-lookup"><span data-stu-id="669f9-145">You can look up those ID numbers in [Image Property Tag Constants](-gdiplus-constant-image-property-tag-constants.md) and find out that they represent the following property tags.</span></span>



| <span data-ttu-id="669f9-146">Hexadezimalwert</span><span class="sxs-lookup"><span data-stu-id="669f9-146">Hexadecimal value</span></span>                                                                                                       | <span data-ttu-id="669f9-147">Eigenschaftstag</span><span class="sxs-lookup"><span data-stu-id="669f9-147">Property tag</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="669f9-148">0x0320 0x010F</span><span class="sxs-lookup"><span data-stu-id="669f9-148">0x0320 0x010f</span></span><br/>  <span data-ttu-id="669f9-149">0x0110</span><span class="sxs-lookup"><span data-stu-id="669f9-149">0x0110</span></span><br/>  <span data-ttu-id="669f9-150">0x9003</span><span class="sxs-lookup"><span data-stu-id="669f9-150">0x9003</span></span><br/>  <span data-ttu-id="669f9-151">0x829a</span><span class="sxs-lookup"><span data-stu-id="669f9-151">0x829a</span></span><br/>  <span data-ttu-id="669f9-152">0x5090</span><span class="sxs-lookup"><span data-stu-id="669f9-152">0x5090</span></span><br/>  <span data-ttu-id="669f9-153">0x5091</span><span class="sxs-lookup"><span data-stu-id="669f9-153">0x5091</span></span><br/> | <span data-ttu-id="669f9-154">Propertytagimagetitle propertytagequipmake</span><span class="sxs-lookup"><span data-stu-id="669f9-154">PropertyTagImageTitle PropertyTagEquipMake</span></span><br/>  <span data-ttu-id="669f9-155">Propertytagequipmodel</span><span class="sxs-lookup"><span data-stu-id="669f9-155">PropertyTagEquipModel</span></span><br/>  <span data-ttu-id="669f9-156">Propertytagexif-Original</span><span class="sxs-lookup"><span data-stu-id="669f9-156">PropertyTagExifDTOriginal</span></span><br/>  <span data-ttu-id="669f9-157">Propertytagexif ExposureTime</span><span class="sxs-lookup"><span data-stu-id="669f9-157">PropertyTagExifExposureTime</span></span><br/>  <span data-ttu-id="669f9-158">Propertytagluminancetable</span><span class="sxs-lookup"><span data-stu-id="669f9-158">PropertyTagLuminanceTable</span></span><br/>  <span data-ttu-id="669f9-159">Propertytagchrominancetable</span><span class="sxs-lookup"><span data-stu-id="669f9-159">PropertyTagChrominanceTable</span></span><br/> |



 

<span data-ttu-id="669f9-160">Das zweite (Index 1)-Eigenschaften Element in der Liste enthält die **ID** propertytagequipmake und den **Typ** propertytagtybäuercii.</span><span class="sxs-lookup"><span data-stu-id="669f9-160">The second (index 1) property item in the list has **id** PropertyTagEquipMake and **type** PropertyTagTypeASCII.</span></span> <span data-ttu-id="669f9-161">Im folgenden Beispiel, bei dem es sich um eine Fortsetzung der vorherigen Konsolenanwendung handelt, wird der Wert dieses Eigenschaften Elements angezeigt:</span><span class="sxs-lookup"><span data-stu-id="669f9-161">The following example, which is a continuation of the previous console application, displays the value of that property item:</span></span>


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



<span data-ttu-id="669f9-162">Die vorherige Codezeile erzeugt die folgende Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="669f9-162">The preceding line of code produces the following output:</span></span>


```
The equipment make is Northwind Traders.
```



<span data-ttu-id="669f9-163">Das fünfte (Index 4)-Eigenschaften Element in der Liste verfügt über die **ID** propertytagexif ExposureTime und den **Typ** propertytagtyperational.</span><span class="sxs-lookup"><span data-stu-id="669f9-163">The fifth (index 4) property item in the list has **id** PropertyTagExifExposureTime and **type** PropertyTagTypeRational.</span></span> <span data-ttu-id="669f9-164">Dieser Datentyp (propertytagtyperational) ist ein paar von **Long** s.</span><span class="sxs-lookup"><span data-stu-id="669f9-164">That data type (PropertyTagTypeRational) is a pair of **LONG** s.</span></span> <span data-ttu-id="669f9-165">Im folgenden Beispiel, bei dem es sich um eine Fortsetzung der vorherigen Konsolenanwendung handelt, werden diese beiden **langen** Werte als Bruchteil angezeigt.</span><span class="sxs-lookup"><span data-stu-id="669f9-165">The following example, which is a continuation of the previous console application, displays those two **LONG** values as a fraction.</span></span> <span data-ttu-id="669f9-166">Dieser Bruchteil, 1/125, ist die in Sekunden gemessene Expositionszeit.</span><span class="sxs-lookup"><span data-stu-id="669f9-166">That fraction, 1/125, is the exposure time measured in seconds.</span></span>


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



<span data-ttu-id="669f9-167">Der oben genannte Code erzeugt die folgende Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="669f9-167">The preceding code produces the following output:</span></span>


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a><span data-ttu-id="669f9-168">Schreiben von Metadaten in eine Datei</span><span class="sxs-lookup"><span data-stu-id="669f9-168">Writing Metadata to a File</span></span>

<span data-ttu-id="669f9-169">Um ein Element von Metadaten in ein [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekt zu schreiben, initialisieren Sie ein [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) -Objekt, und übergeben Sie dann die Adresse dieses **PropertyItem** -Objekts an die **SetPropertyItem** -Methode des **Image** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="669f9-169">To write an item of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, initialize a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object and then pass the address of that **PropertyItem** object to the **SetPropertyItem** method of the **Image** object.</span></span>

<span data-ttu-id="669f9-170">Die folgende Konsolenanwendung schreibt ein Element (den Bildtitel) der Metadaten in ein [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekt und speichert das Bild dann in der Datenträger Datei FakePhoto2.jpg.</span><span class="sxs-lookup"><span data-stu-id="669f9-170">The following console application writes one item (the image title) of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and then saves the image in the disk file FakePhoto2.jpg.</span></span> <span data-ttu-id="669f9-171">Die Main-Funktion basiert auf der-Hilfsfunktion getencoderclsid, die im Thema [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="669f9-171">The main function relies on the helper function GetEncoderClsid, which is shown in the topic [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   Status stat;
   CLSID  clsid;
   char   propertyValue[] = "Fake Photograph";
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   PropertyItem* propertyItem = new PropertyItem;
   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &clsid);
   propertyItem->id = PropertyTagImageTitle;
   propertyItem->length = 16;  // string length including NULL terminator
   propertyItem->type = PropertyTagTypeASCII; 
   propertyItem->value = propertyValue;
   bitmap->SetPropertyItem(propertyItem);
   stat = bitmap->Save(L"FakePhoto2.jpg", &clsid, NULL);
   if(stat == Ok)
      printf("FakePhoto2.jpg saved successfully.\n");
   
   delete propertyItem;
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
