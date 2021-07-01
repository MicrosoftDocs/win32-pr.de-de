---
description: Einige Bilddateien enthalten Metadaten, die Sie lesen können, um Die Features des Bilds zu bestimmen.
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: Lesen und Schreiben von Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4ea0a8f389f31870b31a0b15480815bdd7cf1f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118295"
---
# <a name="reading-and-writing-metadata"></a><span data-ttu-id="8d318-103">Lesen und Schreiben von Metadaten</span><span class="sxs-lookup"><span data-stu-id="8d318-103">Reading and Writing Metadata</span></span>

<span data-ttu-id="8d318-104">Einige Bilddateien enthalten Metadaten, die Sie lesen können, um Die Features des Bilds zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8d318-104">Some image files contain metadata that you can read to determine features of the image.</span></span> <span data-ttu-id="8d318-105">Beispielsweise kann ein digitales Foto Metadaten enthalten, die Sie lesen können, um den Make und das Modell der Kamera zu bestimmen, die zum Erfassen des Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d318-105">For example, a digital photograph might contain metadata that you can read to determine the make and model of the camera used to capture the image.</span></span> <span data-ttu-id="8d318-106">Mit Windows GDI+ können Sie vorhandene Metadaten lesen und auch neue Metadaten in Bilddateien schreiben.</span><span class="sxs-lookup"><span data-stu-id="8d318-106">With Windows GDI+, you can read existing metadata, and you can also write new metadata to image files.</span></span>

<span data-ttu-id="8d318-107">GDI+ bietet eine einheitliche Möglichkeit zum Speichern und Abrufen von Metadaten aus Bilddateien in verschiedenen Formaten.</span><span class="sxs-lookup"><span data-stu-id="8d318-107">GDI+ provides a uniform way of storing and retrieving metadata from image files in various formats.</span></span> <span data-ttu-id="8d318-108">In GDI+ wird ein Metadatenelement als *Eigenschaftenelement bezeichnet.*</span><span class="sxs-lookup"><span data-stu-id="8d318-108">In GDI+, a piece of metadata is called a *property item*.</span></span> <span data-ttu-id="8d318-109">Sie können Metadaten speichern und abrufen, indem Sie die **Methoden SetPropertyItem** und **GetPropertyItem** der [**Image-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) aufrufen, und Sie müssen sich keine Sorgen darüber machen, wie diese Metadaten in einem bestimmten Dateiformat gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="8d318-109">You can store and retrieve metadata by calling the **SetPropertyItem** and **GetPropertyItem** methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned about the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="8d318-110">GDI+ unterstützt derzeit Metadaten für die Dateiformate TIFF, JPEG, Exif und PNG.</span><span class="sxs-lookup"><span data-stu-id="8d318-110">GDI+ currently supports metadata for the TIFF, JPEG, Exif, and PNG file formats.</span></span> <span data-ttu-id="8d318-111">Das Exif-Format, das angibt, wie von digitalen Kameras erfasste Bilder gespeichert werden, baut auf den TIFF- und JPEG-Formaten auf.</span><span class="sxs-lookup"><span data-stu-id="8d318-111">The Exif format, which specifies how to store images captured by digital still cameras, is built on top of the TIFF and JPEG formats.</span></span> <span data-ttu-id="8d318-112">Exif verwendet das TIFF-Format für unkomprimierte Pixeldaten und das JPEG-Format für komprimierte Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="8d318-112">Exif uses the TIFF format for uncompressed pixel data and the JPEG format for compressed pixel data.</span></span>

<span data-ttu-id="8d318-113">GDI+ definiert einen Satz von Eigenschaftstags, die Eigenschaftenelemente identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8d318-113">GDI+ defines a set of property tags that identify property items.</span></span> <span data-ttu-id="8d318-114">Bestimmte Tags sind allgemein. Das heißt, sie werden von allen Dateiformaten unterstützt, die im vorherigen Absatz erwähnt werden.</span><span class="sxs-lookup"><span data-stu-id="8d318-114">Certain tags are general-purpose; that is, they are supported by all of the file formats mentioned in the preceding paragraph.</span></span> <span data-ttu-id="8d318-115">Andere Tags sind speziell und gelten nur für bestimmte Formate.</span><span class="sxs-lookup"><span data-stu-id="8d318-115">Other tags are special-purpose and apply only to certain formats.</span></span> <span data-ttu-id="8d318-116">Wenn Sie versuchen, ein Eigenschaftenelement in einer Datei zu speichern, die dieses Eigenschaftenelement nicht unterstützt, ignoriert GDI+ die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8d318-116">If you try to save a property item to a file that does not support that property item, GDI+ ignores the request.</span></span> <span data-ttu-id="8d318-117">Genauer gesagt gibt die [**Image::SetPropertyItem-Methode**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) PropertyNotSupported zurück.</span><span class="sxs-lookup"><span data-stu-id="8d318-117">More specifically, the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) method returns PropertyNotSupported.</span></span>

<span data-ttu-id="8d318-118">Sie können die Eigenschaftenelemente bestimmen, die in einer Bilddatei gespeichert sind, indem Sie [**Image::GetPropertyIdList aufrufen.**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist)</span><span class="sxs-lookup"><span data-stu-id="8d318-118">You can determine the property items that are stored in an image file by calling [**Image::GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span></span> <span data-ttu-id="8d318-119">Wenn Sie versuchen, ein Eigenschaftenelement abzurufen, das sich nicht in der Datei befindet, ignoriert GDI+ die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8d318-119">If you try to retrieve a property item that is not in the file, GDI+ ignores the request.</span></span> <span data-ttu-id="8d318-120">Genauer gesagt gibt die [**Image::GetPropertyItem-Methode**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) PropertyNotFound zurück.</span><span class="sxs-lookup"><span data-stu-id="8d318-120">More specifically, the [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) method returns PropertyNotFound.</span></span>

## <a name="reading-metadata-from-a-file"></a><span data-ttu-id="8d318-121">Lesen von Metadaten aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="8d318-121">Reading Metadata from a File</span></span>

<span data-ttu-id="8d318-122">Die folgende Konsolenanwendung ruft die **GetPropertySize-Methode** eines [**Image-Objekts**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) auf, um zu bestimmen, wie viele Metadaten in der Datei enthalten FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="8d318-122">The following console application calls the **GetPropertySize** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object to determine how many pieces of metadata are in the file FakePhoto.jpg.</span></span>


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



<span data-ttu-id="8d318-123">Der vorangehende Code hat zusammen mit einer bestimmten Datei, FakePhoto.jpg, die folgende Ausgabe erzeugt:</span><span class="sxs-lookup"><span data-stu-id="8d318-123">The preceding code, along with a particular file, FakePhoto.jpg, produced the following output:</span></span>


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



<span data-ttu-id="8d318-124">GDI+ speichert einzelne Metadaten in einem [**PropertyItem-Objekt.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem)</span><span class="sxs-lookup"><span data-stu-id="8d318-124">GDI+ stores an individual piece of metadata in a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object.</span></span> <span data-ttu-id="8d318-125">Sie können die **GetAllPropertyItems-Methode** der [**Image-Klasse aufrufen,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) um alle Metadaten aus einer Datei abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8d318-125">You can call the **GetAllPropertyItems** method of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class to retrieve all the metadata from a file.</span></span> <span data-ttu-id="8d318-126">Die **GetAllPropertyItems-Methode** gibt ein Array von **PropertyItem-Objekten** zurück.</span><span class="sxs-lookup"><span data-stu-id="8d318-126">The **GetAllPropertyItems** method returns an array of **PropertyItem** objects.</span></span> <span data-ttu-id="8d318-127">Bevor Sie **GetAllPropertyItems** aufrufen, müssen Sie einen Puffer zuordnen, der groß genug ist, um dieses Array zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="8d318-127">Before you call **GetAllPropertyItems**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="8d318-128">Sie können die **GetPropertySize-Methode** der **Image-Klasse** aufrufen, um die Größe (in Bytes) des erforderlichen Puffers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8d318-128">You can call the **GetPropertySize** method of the **Image** class to get the size (in bytes) of the required buffer.</span></span>

<span data-ttu-id="8d318-129">Ein [**PropertyItem-Objekt**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) verfügt über die folgenden vier öffentlichen Member:</span><span class="sxs-lookup"><span data-stu-id="8d318-129">A [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object has the following four public members:</span></span>



|            | <span data-ttu-id="8d318-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d318-130">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d318-131">**id**</span><span class="sxs-lookup"><span data-stu-id="8d318-131">**id**</span></span>     | <span data-ttu-id="8d318-132">Ein Tag, das das Metadatenelement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8d318-132">A tag that identifies the metadata item.</span></span> <span data-ttu-id="8d318-133">Die Werte, die der **ID** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime und derEntität) zugewiesen werden können, werden in "Gdiplusimaging.h" definiert.</span><span class="sxs-lookup"><span data-stu-id="8d318-133">The values that can be assigned to **id** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime, and the like) are defined in Gdiplusimaging.h.</span></span>                                                                                           |
| <span data-ttu-id="8d318-134">**length**</span><span class="sxs-lookup"><span data-stu-id="8d318-134">**length**</span></span> | <span data-ttu-id="8d318-135">Die Länge des Arrays von Werten in Bytes, auf das der Wertdaten **member** zeigt.</span><span class="sxs-lookup"><span data-stu-id="8d318-135">The length, in bytes, of the array of values pointed to by the **value** data member.</span></span> <span data-ttu-id="8d318-136">Beachten Sie:  Wenn der Typdaten member auf PropertyTagTypeASCII festgelegt  ist, ist der Längendaten member die Länge einer auf NULL endbaren Zeichenfolge, einschließlich des NULL-Abschlusszeichens.</span><span class="sxs-lookup"><span data-stu-id="8d318-136">Note that if the **type** data member is set to PropertyTagTypeASCII, then the length data member is the **length** of a null-terminated character string, including the NULL terminator.</span></span>                        |
| <span data-ttu-id="8d318-137">**type**</span><span class="sxs-lookup"><span data-stu-id="8d318-137">**type**</span></span>   | <span data-ttu-id="8d318-138">Der Datentyp der Werte im Array, auf die der Wertdaten member zeigt.</span><span class="sxs-lookup"><span data-stu-id="8d318-138">The data type of the values in the array pointed to by the value data member.</span></span> <span data-ttu-id="8d318-139">Konstanten (PropertyTagTypeByte, PropertyTagTypeASCII und deren Art), die verschiedene Datentypen darstellen, werden unter [**Image Property Tag Type Constants beschrieben.**](-gdiplus-constant-image-property-tag-type-constants.md)</span><span class="sxs-lookup"><span data-stu-id="8d318-139">Constants (PropertyTagTypeByte, PropertyTagTypeASCII, and the like) that represent various data types are described in [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span> |
| <span data-ttu-id="8d318-140">**value**</span><span class="sxs-lookup"><span data-stu-id="8d318-140">**value**</span></span>  | <span data-ttu-id="8d318-141">Ein Zeiger auf ein Array von Werten.</span><span class="sxs-lookup"><span data-stu-id="8d318-141">A pointer to an array of values.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="8d318-142">Die folgende Konsolenanwendung liest die sieben Metadaten in der Datei und zeigt sie FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="8d318-142">The following console application reads and displays the seven pieces of metadata in the file FakePhoto.jpg.</span></span> <span data-ttu-id="8d318-143">Die main-Funktion basiert auf der Hilfsfunktion PropertyTypeFromWORD, die nach der main-Funktion angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8d318-143">The main function relies on the helper function PropertyTypeFromWORD, which is shown following the main function.</span></span>


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



<span data-ttu-id="8d318-144">Die obige Konsolenanwendung erzeugt die folgende Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="8d318-144">The preceding console application produces the following output:</span></span>


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



<span data-ttu-id="8d318-145">In der obigen Ausgabe wird eine hexadezimale ID-Nummer für jedes Eigenschaftenelement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d318-145">The preceding output shows a hexadecimal ID number for each property item.</span></span> <span data-ttu-id="8d318-146">Sie können diese ID-Nummern in [Image Property Tag Constants](-gdiplus-constant-image-property-tag-constants.md) nachschlagen und feststellen, dass sie die folgenden Eigenschaftstags darstellen.</span><span class="sxs-lookup"><span data-stu-id="8d318-146">You can look up those ID numbers in [Image Property Tag Constants](-gdiplus-constant-image-property-tag-constants.md) and find out that they represent the following property tags.</span></span>



| <span data-ttu-id="8d318-147">Hexadezimalwert</span><span class="sxs-lookup"><span data-stu-id="8d318-147">Hexadecimal value</span></span>                                                                                                       | <span data-ttu-id="8d318-148">Eigenschaftentag</span><span class="sxs-lookup"><span data-stu-id="8d318-148">Property tag</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d318-149">0x0320 0x010f</span><span class="sxs-lookup"><span data-stu-id="8d318-149">0x0320 0x010f</span></span><br/>  <span data-ttu-id="8d318-150">0x0110</span><span class="sxs-lookup"><span data-stu-id="8d318-150">0x0110</span></span><br/>  <span data-ttu-id="8d318-151">0x9003</span><span class="sxs-lookup"><span data-stu-id="8d318-151">0x9003</span></span><br/>  <span data-ttu-id="8d318-152">0x829a</span><span class="sxs-lookup"><span data-stu-id="8d318-152">0x829a</span></span><br/>  <span data-ttu-id="8d318-153">0x5090</span><span class="sxs-lookup"><span data-stu-id="8d318-153">0x5090</span></span><br/>  <span data-ttu-id="8d318-154">0x5091</span><span class="sxs-lookup"><span data-stu-id="8d318-154">0x5091</span></span><br/> | <span data-ttu-id="8d318-155">PropertyTagImageTitle-EigenschaftTagEquipMake</span><span class="sxs-lookup"><span data-stu-id="8d318-155">PropertyTagImageTitle PropertyTagEquipMake</span></span><br/>  <span data-ttu-id="8d318-156">PropertyTagEquipModel</span><span class="sxs-lookup"><span data-stu-id="8d318-156">PropertyTagEquipModel</span></span><br/>  <span data-ttu-id="8d318-157">PropertyTagExifDTOriginal</span><span class="sxs-lookup"><span data-stu-id="8d318-157">PropertyTagExifDTOriginal</span></span><br/>  <span data-ttu-id="8d318-158">PropertyTagExifExposureTime</span><span class="sxs-lookup"><span data-stu-id="8d318-158">PropertyTagExifExposureTime</span></span><br/>  <span data-ttu-id="8d318-159">PropertyTagLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="8d318-159">PropertyTagLuminanceTable</span></span><br/>  <span data-ttu-id="8d318-160">PropertyTagChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="8d318-160">PropertyTagChrominanceTable</span></span><br/> |



 

<span data-ttu-id="8d318-161">Das zweite Eigenschaftenelement (Index 1) in der Liste hat **die ID** PropertyTagEquipMake und **den** Typ PropertyTagTypeASCII.</span><span class="sxs-lookup"><span data-stu-id="8d318-161">The second (index 1) property item in the list has **id** PropertyTagEquipMake and **type** PropertyTagTypeASCII.</span></span> <span data-ttu-id="8d318-162">Im folgenden Beispiel, bei dem es sich um eine Fortsetzung der vorherigen Konsolenanwendung handelt, wird der Wert dieses Eigenschaftenelements angezeigt:</span><span class="sxs-lookup"><span data-stu-id="8d318-162">The following example, which is a continuation of the previous console application, displays the value of that property item:</span></span>


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



<span data-ttu-id="8d318-163">Die vorangehende Codezeile erzeugt die folgende Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="8d318-163">The preceding line of code produces the following output:</span></span>


```
The equipment make is Northwind Traders.
```



<span data-ttu-id="8d318-164">Das fünfte Eigenschaftenelement (Index 4) in der Liste hat **die ID** PropertyTagExifExposureTime und **den** Typ PropertyTagTypeRational.</span><span class="sxs-lookup"><span data-stu-id="8d318-164">The fifth (index 4) property item in the list has **id** PropertyTagExifExposureTime and **type** PropertyTagTypeRational.</span></span> <span data-ttu-id="8d318-165">Dieser Datentyp (PropertyTagTypeRational) ist ein Paar **von LONG-s.**</span><span class="sxs-lookup"><span data-stu-id="8d318-165">That data type (PropertyTagTypeRational) is a pair of **LONG** s.</span></span> <span data-ttu-id="8d318-166">Im folgenden Beispiel, bei dem es sich um eine Fortsetzung der vorherigen Konsolenanwendung handelt, werden diese beiden **LONG-Werte** als Bruch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d318-166">The following example, which is a continuation of the previous console application, displays those two **LONG** values as a fraction.</span></span> <span data-ttu-id="8d318-167">Dieser Bruchteil (1/125) ist die in Sekunden gemessene Belichtungszeit.</span><span class="sxs-lookup"><span data-stu-id="8d318-167">That fraction, 1/125, is the exposure time measured in seconds.</span></span>


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



<span data-ttu-id="8d318-168">Der oben genannte Code erzeugt die folgende Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="8d318-168">The preceding code produces the following output:</span></span>


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a><span data-ttu-id="8d318-169">Schreiben von Metadaten in eine Datei</span><span class="sxs-lookup"><span data-stu-id="8d318-169">Writing Metadata to a File</span></span>

<span data-ttu-id="8d318-170">Initialisieren Sie zum Schreiben eines Metadatenelements in ein [**Image-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) ein [**PropertyItem-Objekt,**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) und übergeben Sie dann die Adresse dieses **PropertyItem-Objekts** an die **SetPropertyItem-Methode** des **Image-Objekts.**</span><span class="sxs-lookup"><span data-stu-id="8d318-170">To write an item of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, initialize a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object and then pass the address of that **PropertyItem** object to the **SetPropertyItem** method of the **Image** object.</span></span>

<span data-ttu-id="8d318-171">Die folgende Konsolenanwendung schreibt ein Element (den Bildtitel) der Metadaten in ein [**Image-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) und speichert das Image dann in der Datenträgerdatei FakePhoto2.jpg.</span><span class="sxs-lookup"><span data-stu-id="8d318-171">The following console application writes one item (the image title) of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and then saves the image in the disk file FakePhoto2.jpg.</span></span> <span data-ttu-id="8d318-172">Die main-Funktion basiert auf der Hilfsfunktion GetEncoderClsid, die im Thema Abrufen des Klassenbezeichners für einen [Encoder gezeigt wird.](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)</span><span class="sxs-lookup"><span data-stu-id="8d318-172">The main function relies on the helper function GetEncoderClsid, which is shown in the topic [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 
