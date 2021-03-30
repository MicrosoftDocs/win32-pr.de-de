---
description: 'Die Image-Klasse stellt die Image:: GetEncoderParameterList-Methode bereit, sodass Sie die Parameter ermitteln können, die von einem bestimmten Bild Encoder unterstützt werden.'
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: Bestimmen der von einem Encoder unterstützten Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9bd76abb0b9f01bf55fd738df77cd086bc757c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994279"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a>Bestimmen der von einem Encoder unterstützten Parameter

Die [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse stellt die [**Image:: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) -Methode bereit, sodass Sie die Parameter ermitteln können, die von einem bestimmten Bild Encoder unterstützt werden. Die **Image:: GetEncoderParameterList** -Methode gibt ein Array von [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekten zurück. Vor dem Aufrufen von **Image:: GetEncoderParameterList** müssen Sie einen Puffer zuordnen, um das Array zu erhalten. Sie können " [**Image:: getencoderparameterlistsize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) " aufrufen, um die Größe des erforderlichen Puffers zu bestimmen.

Die folgende Konsolenanwendung ruft die Parameterliste für den JPEG-Encoder ab. Die Main-Funktion basiert auf der-Hilfsfunktion getencoderclsid, die unter [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)angezeigt wird.


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   // Create Bitmap (inherited from Image) object so that we can call
   // GetParameterListSize and GetParameterList.
   Bitmap* bitmap = new Bitmap(1, 1);

   // Get the JPEG encoder CLSID.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // How big (in bytes) is the JPEG encoder's parameter list?
   UINT listSize = 0; 
   listSize = bitmap->GetEncoderParameterListSize(&encoderClsid);
   printf("The parameter list requires %d bytes.\n", listSize);

   // Allocate a buffer large enough to hold the parameter list.
   EncoderParameters* pEncoderParameters = NULL;
   pEncoderParameters = (EncoderParameters*)malloc(listSize);

   // Get the parameter list for the JPEG encoder.
   bitmap->GetEncoderParameterList(
      &encoderClsid, listSize, pEncoderParameters);

   // pEncoderParameters points to an EncoderParameters object, which
   // has a Count member and an array of EncoderParameter objects.
   // How many EncoderParameter objects are in the array?
   printf("There are %d EncoderParameter objects in the array.\n", 
      pEncoderParameters->Count);

   free(pEncoderParameters);
   delete(bitmap);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Wenn Sie die vorherige Konsolenanwendung ausführen, erhalten Sie eine Ausgabe wie die folgende:


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



Jedes der [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekte im Array verfügt über die folgenden vier öffentlichen Datenmember:

Der folgende Code ist eine Fortsetzung der Konsolenanwendung, die im vorherigen Beispiel gezeigt wird. Der Code untersucht das zweite [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekt im Array, das von [**Image:: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist)zurückgegeben wurde. Der Code ruft [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2)auf, bei dem es sich um eine Systemfunktion handelt, die in objbase. h deklariert ist, um den **GUID** -Member des **EncoderParameter** -Objekts in eine Zeichenfolge zu konvertieren.


```
// Look at the second (index 1) EncoderParameter object in the array.
printf("Parameter[1]\n");

WCHAR strGuid[39];
StringFromGUID2(pEncoderParameters->Parameter[1].Guid, strGuid, 39);
wprintf(L"   The GUID is %s.\n", strGuid);

printf("   The value type is %d.\n", 
   pEncoderParameters->Parameter[1].Type);

printf("   The number of values is %d.\n",
   pEncoderParameters->Parameter[1].NumberOfValues);
```



Der oben genannte Code erzeugt die folgende Ausgabe:


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



Sie können die GUID in "gdiplusimaging. h" nachschlagen und herausfinden, dass die Kategorie dieses [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekts "encoderquality" ist. Sie können diese Kategorie (encoderquality) des Parameters verwenden, um die Komprimierungs Ebene eines JPEG-Bilds festzulegen.

In gdiplusenums. h gibt die [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) -Enumeration an, dass der Datentyp 6 **valuelongrange** ist. Ein langer Bereich ist ein paar von **ulong** -Werten.

Die Anzahl der Werte ist 1. daher wissen wir, dass der **Wertmember** des [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekts ein Zeiger auf ein Array mit einem Element ist. Ein Element ist ein paar von **ulong** -Werten.

Der folgende Code ist eine Fortsetzung der Konsolenanwendung, die in den vorherigen beiden Beispielen gezeigt wird. Der Code definiert einen Datentyp namens **plongrange** (Zeiger auf einen langen Bereich). Eine Variable vom Typ **plongrange** wird verwendet, um die Mindest-und Höchstwerte zu extrahieren, die als Qualitätseinstellung an den JPEG-Encoder übermittelt werden können.


```
typedef struct
   {
      long min;
      long max;
   }* PLONGRANGE;

   PLONGRANGE pLongRange = 
      (PLONGRANGE)(pEncoderParameters->Parameter[1].Value);

   printf("   The minimum possible quality value is %d.\n",
      pLongRange->min);

   printf("   The maximum possible quality value is %d.\n",
      pLongRange->max);
```



Der oben genannte Code erzeugt die folgende Ausgabe:


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



Im vorherigen Beispiel ist der Wert, der im [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekt zurückgegeben wird, ein paar von **ulong** -Werten, die die minimalen und maximalen möglichen Werte für den Quality-Parameter angeben. In einigen Fällen sind die Werte, die in einem **EncoderParameter** -Objekt zurückgegeben werden, Member der [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) -Enumeration. In den folgenden Themen werden die **EncoderValue** -Enumeration und Methoden zum Auflisten möglicher Parameterwerte ausführlicher erläutert:

-   [Verwenden der EncoderValue-Enumeration](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [Auflisten von Parametern und Werten für alle Encoder](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 
