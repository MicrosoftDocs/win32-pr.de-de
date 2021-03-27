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
# <a name="reading-and-writing-metadata"></a>Lesen und Schreiben von Metadaten

Einige Bilddateien enthalten Metadaten, die Sie lesen können, um die Funktionen des Images zu ermitteln. Beispielsweise kann ein digitales Foto Metadaten enthalten, die Sie lesen können, um die Marke und das Modell der Kamera zu ermitteln, die zum Erfassen des Bilds verwendet wird. Mit Windows GDI+ können Sie vorhandene Metadaten lesen, und Sie können auch neue Metadaten in Bilddateien schreiben.

GDI+ bietet eine einheitliche Möglichkeit zum Speichern und Abrufen von Metadaten aus Bilddateien in verschiedenen Formaten. In GDI+ wird ein *Metadatenelement als Eigenschaften Element* bezeichnet. Sie können Metadaten speichern und abrufen, indem Sie die **SetPropertyItem** -Methode und die **GetPropertyItem** -Methode der [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse aufrufen, und Sie müssen sich nicht um die Details kümmern, wie ein bestimmtes Dateiformat diese Metadaten speichert.

GDI+ unterstützt derzeit Metadaten für die Dateiformate TIFF, JPEG, EXIF und PNG. Das EXIF-Format, das angibt, wie von digitalen Digitalkameras erfasste Bilder gespeichert werden, basiert auf den TIFF-und JPEG-Formaten. EXIF verwendet das TIFF-Format für unkomprimierte Pixeldaten und das JPEG-Format für komprimierte Pixeldaten.

GDI+ definiert einen Satz von Eigenschafts Tags, die Eigenschaften Elemente identifizieren. Bestimmte Tags sind universell. Das heißt, Sie werden von allen Dateiformaten unterstützt, die im vorherigen Abschnitt erwähnt wurden. Andere Tags sind besondere Zwecke und gelten nur für bestimmte Formate. Wenn Sie versuchen, ein Eigenschaften Element in einer Datei zu speichern, die dieses Eigenschaften Element nicht unterstützt, wird die Anforderung von GDI+ ignoriert. Genauer gesagt gibt die [**Image:: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) -Methode propertynotsupported zurück.

Sie können die Eigenschaften Elemente, die in einer Bilddatei gespeichert sind, durch Aufrufen von " [**Image:: getpropertyidlist**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist)" ermitteln. Wenn Sie versuchen, ein Eigenschaften Element abzurufen, das sich nicht in der Datei befindet, wird die Anforderung von GDI+ ignoriert. Genauer gesagt gibt die [**Image:: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) -Methode propertynotfound zurück.

## <a name="reading-metadata-from-a-file"></a>Lesen von Metadaten aus einer Datei

Die folgende Konsolenanwendung ruft die **getpropertysize** -Methode eines [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekts auf, um zu bestimmen, wie viele Metadaten in der Datei FakePhoto.jpg sind.


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



Der vorangehende Code hat zusammen mit einer bestimmten Datei FakePhoto.jpg die folgende Ausgabe erzeugt:


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



GDI+ speichert ein einzelnes Metadatenelement in einem [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) -Objekt. Sie können die **getallpropertyitems** -Methode der [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse aufrufen, um alle Metadaten aus einer Datei abzurufen. Die **getallpropertyitems** -Methode gibt ein Array von **PropertyItem** -Objekten zurück. Vor dem Aufrufen von **getallpropertyitems** müssen Sie einen Puffer zuordnen, der groß genug ist, um das Array zu erhalten. Sie können die **getpropertysize** -Methode der **Image** -Klasse aufrufen, um die Größe (in Bytes) des erforderlichen Puffers zu erhalten.

Ein [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) -Objekt verfügt über die folgenden vier öffentlichen Member:



|            |                                                                                                                                                                                                                                                                                                        |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **id**     | Ein-Tag, das das Metadatenelement bezeichnet. Die Werte, die **ID** zugewiesen werden können (propertytagimagetitle, propertytagequipmake, propertytagexifexposuretime und like), werden in gdiplusimaging. h definiert.                                                                                           |
| **length** | Die Länge (in Byte) des Arrays von Werten, auf die vom **wertdatenmember** verwiesen wird. Beachten Sie Folgendes: Wenn das **Typdatenmember** auf propertytagtybäuercii festgelegt ist, ist das length-Datenmember die **Länge** einer null-terminierten Zeichenfolge, einschließlich des NULL-Terminator.                        |
| **type**   | Der Datentyp der Werte im Array, auf die vom wertdatenmember verwiesen wird. Konstanten (propertytagtypebyte, propertytagtybäuercii und like), die verschiedene Datentypen darstellen, werden in den [**Tagtyp Konstanten des Image-Eigenschaften**](-gdiplus-constant-image-property-tag-type-constants.md)beschrieben. |
| **value**  | Ein Zeiger auf ein Array von-Werten.                                                                                                                                                                                                                                                                       |



 

Die folgende Konsolenanwendung liest und zeigt die sieben Metadatenelemente in der Datei FakePhoto.jpg an. Die Main-Funktion basiert auf der Hilfsfunktion propertytypefromword, die nach der Main-Funktion angezeigt wird.


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



Die vorherige Konsolenanwendung erzeugt die folgende Ausgabe:


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



Die obige Ausgabe zeigt eine hexadezimale ID-Nummer für jedes Eigenschafts Element an. Sie können diese ID-Nummern in den [tagkonstanten der Abbild Eigenschaften](-gdiplus-constant-image-property-tag-constants.md) nachschlagen und ermitteln, dass Sie die folgenden Eigenschaften Tags darstellen.



| Hexadezimalwert                                                                                                       | Eigenschaftstag                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0320 0x010F<br/>  0x0110<br/>  0x9003<br/>  0x829a<br/>  0x5090<br/>  0x5091<br/> | Propertytagimagetitle propertytagequipmake<br/>  Propertytagequipmodel<br/>  Propertytagexif-Original<br/>  Propertytagexif ExposureTime<br/>  Propertytagluminancetable<br/>  Propertytagchrominancetable<br/> |



 

Das zweite (Index 1)-Eigenschaften Element in der Liste enthält die **ID** propertytagequipmake und den **Typ** propertytagtybäuercii. Im folgenden Beispiel, bei dem es sich um eine Fortsetzung der vorherigen Konsolenanwendung handelt, wird der Wert dieses Eigenschaften Elements angezeigt:


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



Die vorherige Codezeile erzeugt die folgende Ausgabe:


```
The equipment make is Northwind Traders.
```



Das fünfte (Index 4)-Eigenschaften Element in der Liste verfügt über die **ID** propertytagexif ExposureTime und den **Typ** propertytagtyperational. Dieser Datentyp (propertytagtyperational) ist ein paar von **Long** s. Im folgenden Beispiel, bei dem es sich um eine Fortsetzung der vorherigen Konsolenanwendung handelt, werden diese beiden **langen** Werte als Bruchteil angezeigt. Dieser Bruchteil, 1/125, ist die in Sekunden gemessene Expositionszeit.


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



Der oben genannte Code erzeugt die folgende Ausgabe:


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a>Schreiben von Metadaten in eine Datei

Um ein Element von Metadaten in ein [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekt zu schreiben, initialisieren Sie ein [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) -Objekt, und übergeben Sie dann die Adresse dieses **PropertyItem** -Objekts an die **SetPropertyItem** -Methode des **Image** -Objekts.

Die folgende Konsolenanwendung schreibt ein Element (den Bildtitel) der Metadaten in ein [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekt und speichert das Bild dann in der Datenträger Datei FakePhoto2.jpg. Die Main-Funktion basiert auf der-Hilfsfunktion getencoderclsid, die im Thema [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)gezeigt wird.


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



 

 
