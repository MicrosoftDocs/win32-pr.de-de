---
description: Einige Bilddateien enthalten Metadaten, die Sie lesen können, um die Features des Bilds zu bestimmen.
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: Lesen und Schreiben von Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b965285e2d8a4666ef86b78cdc5dbb9ed38c55ee7c84b4a93f1dbe80141efa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114930"
---
# <a name="reading-and-writing-metadata"></a>Lesen und Schreiben von Metadaten

Einige Bilddateien enthalten Metadaten, die Sie lesen können, um die Features des Bilds zu bestimmen. Beispielsweise kann ein digitales Foto Metadaten enthalten, die Sie lesen können, um die Marke und das Modell der Kamera zu bestimmen, die zum Erfassen des Bilds verwendet wird. Mit Windows GDI+ können Sie vorhandene Metadaten lesen und auch neue Metadaten in Bilddateien schreiben.

GDI+ bietet eine einheitliche Möglichkeit zum Speichern und Abrufen von Metadaten aus Bilddateien in verschiedenen Formaten. In GDI+ wird ein Metadatenelement als *Eigenschaftselement* bezeichnet. Sie können Metadaten speichern und abrufen, indem Sie die **Methoden SetPropertyItem** und **GetPropertyItem** der [**Image-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) aufrufen, und Sie müssen sich keine Gedanken darüber machen, wie ein bestimmtes Dateiformat diese Metadaten speichert.

GDI+ unterstützt derzeit Metadaten für die Dateiformate TIFF, JPEG, Exif und PNG. Das Exif-Format, das angibt, wie Bilder gespeichert werden, die von digitalen Standbildkameras erfasst werden, basiert auf den TIFF- und JPEG-Formaten. Exif verwendet das TIFF-Format für unkomprimierte Pixeldaten und das JPEG-Format für komprimierte Pixeldaten.

GDI+ definiert einen Satz von Eigenschaftentags, die Eigenschaftselemente identifizieren. Bestimmte Tags sind allgemein einsetzbar. Das heißt, sie werden von allen dateiformaten unterstützt, die im vorherigen Absatz erwähnt wurden. Andere Tags sind speziell und gelten nur für bestimmte Formate. Wenn Sie versuchen, ein Eigenschaftenelement in einer Datei zu speichern, die dieses Eigenschaftselement nicht unterstützt, ignoriert GDI+ die Anforderung. Genauer gesagt gibt die [**Image::SetPropertyItem-Methode**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) PropertyNotSupported zurück.

Sie können die in einer Bilddatei gespeicherten Eigenschaftenelemente ermitteln, indem [**Sie Image::GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist)aufrufen. Wenn Sie versuchen, ein Eigenschaftenelement abzurufen, das sich nicht in der Datei befindet, ignoriert GDI+ die Anforderung. Genauer gesagt gibt die [**Image::GetPropertyItem-Methode**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) PropertyNotFound zurück.

## <a name="reading-metadata-from-a-file"></a>Lesen von Metadaten aus einer Datei

Die folgende Konsolenanwendung ruft die **GetPropertySize-Methode** eines [**Image-Objekts**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) auf, um zu bestimmen, wie viele Metadaten in der Datei FakePhoto.jpg sind.


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



Der vorangehende Code erzeugt zusammen mit einer bestimmten Datei FakePhoto.jpg die folgende Ausgabe:


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



GDI+ speichert einzelne Metadaten in einem [**PropertyItem-Objekt.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) Sie können die **GetAllPropertyItems-Methode** der [**Image-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) aufrufen, um alle Metadaten aus einer Datei abzurufen. Die **GetAllPropertyItems-Methode** gibt ein Array von **PropertyItem-Objekten** zurück. Bevor Sie **GetAllPropertyItems** aufrufen, müssen Sie einen Puffer zuordnen, der groß genug ist, um dieses Array zu empfangen. Sie können die **GetPropertySize-Methode** der **Image-Klasse** aufrufen, um die Größe (in Bytes) des erforderlichen Puffers abzurufen.

Ein [**PropertyItem-Objekt**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) verfügt über die folgenden vier öffentlichen Member:



|            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                       |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **id**     | Ein Tag, das das Metadatenelement identifiziert. Die Werte, die **id** zugewiesen werden können (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime usw.), werden in Gdiplusimaging.h definiert.                                                                                           |
| **length** | Die Länge des Arrays von Werten in Bytes, auf die der **Wertdatenmember** zeigt. Beachten Sie Folgendes: Wenn der **Typdatenmember** auf PropertyTagTypeASCII festgelegt ist, entspricht der Length-Datenmember der **Länge** einer auf NULL endenden Zeichenfolge, einschließlich des NULL-Abschlusszeichens.                        |
| **type**   | Der Datentyp der Werte im Array, auf das der Wertdatenmember zeigt. Konstanten (PropertyTagTypeByte, PropertyTagTypeASCII und ähnliche), die verschiedene Datentypen darstellen, werden unter [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md)beschrieben. |
| **value**  | Ein Zeiger auf ein Array von Werten.                                                                                                                                                                                                                                                                       |



 

Die folgende Konsolenanwendung liest und zeigt die sieben Metadaten in der Datei FakePhoto.jpg an. Die main-Funktion basiert auf der Hilfsfunktion PropertyTypeFromWORD, die nach der Main-Funktion angezeigt wird.


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



Die vorherige Ausgabe zeigt eine hexadezimale ID-Nummer für jedes Eigenschaftselement. Sie können diese ID-Nummern in [Tagkonstanten](-gdiplus-constant-image-property-tag-constants.md) für Bildeigenschaften nachschlagen und feststellen, dass sie die folgenden Eigenschaftstags darstellen.



| Hexadezimalwert                                                                                                       | Eigenschaftentag                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0320 0x010f<br/>  0x0110<br/>  0x9003<br/>  0x829a<br/>  0x5090<br/>  0x5091<br/> | PropertyTagImageTitle PropertyTagEquipMake<br/>  PropertyTagEquipModel<br/>  PropertyTagExifDTOriginal<br/>  PropertyTagExifExposureTime<br/>  PropertyTagLuminanceTable<br/>  PropertyTagColorinanceTable<br/> |



 

Das zweite Eigenschaftselement (Index 1) in der Liste hat die **ID** PropertyTagEquipMake und **den Typ** PropertyTagTypeASCII. Im folgenden Beispiel, bei dem es sich um eine Fortsetzung der vorherigen Konsolenanwendung handelt, wird der Wert dieses Eigenschaftselements angezeigt:


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



Die vorangehende Codezeile erzeugt die folgende Ausgabe:


```
The equipment make is Northwind Traders.
```



Das fünfte Eigenschaftselement (Index 4) in der Liste hat die **ID** PropertyTagExifExposureTime und **den Typ** PropertyTagTypeRational. Dieser Datentyp (PropertyTagTypeRational) ist ein Paar von **LONG** s. Im folgenden Beispiel, bei dem es sich um eine Fortsetzung der vorherigen Konsolenanwendung handelt, werden diese beiden **LONG-Werte** als Bruch angezeigt. Dieser Bruchteil (1/125) ist die in Sekunden gemessene Belichtungszeit.


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



Der oben genannte Code erzeugt die folgende Ausgabe:


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a>Schreiben von Metadaten in eine Datei

Um ein Element mit Metadaten in ein [**Image-Objekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) zu schreiben, initialisieren Sie ein [**PropertyItem-Objekt**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) und übergeben dann die Adresse dieses **PropertyItem-Objekts** an die **SetPropertyItem-Methode** des **Image-Objekts.**

Die folgende Konsolenanwendung schreibt ein Element (den Imagetitel) von Metadaten in ein [**Imageobjekt**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) und speichert das Image dann in der Datenträgerdatei FakePhoto2.jpg. Die main-Funktion basiert auf der Hilfsfunktion GetEncoderClsid, die im Thema [Abrufen des Klassenbezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)gezeigt wird.


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



 

 
