---
description: Die Image-Klasse stellt die Image::GetEncoderParameterList-Methode zur Auswahl, damit Sie die Parameter bestimmen können, die von einem bestimmten Bildencoder unterstützt werden.
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: Bestimmen der von einem Encoder unterstützten Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c842b14a2d14af578eede428e79018a2d266ea6133ed61a9bd0736e8dadc97e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977570"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a>Bestimmen der von einem Encoder unterstützten Parameter

Die [**Image-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) stellt die [**Image::GetEncoderParameterList-Methode**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) zur Auswahl, damit Sie die Parameter bestimmen können, die von einem bestimmten Bildencoder unterstützt werden. Die **Image::GetEncoderParameterList-Methode gibt** ein Array von [**EncoderParameter-Objekten**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) zurück. Sie müssen einen Puffer zuordnen, um dieses Array zu empfangen, bevor Sie **Image::GetEncoderParameterList aufrufen.** Sie können [**Image::GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) aufrufen, um die Größe des erforderlichen Puffers zu bestimmen.

Die folgende Konsolenanwendung erhält die Parameterliste für den JPEG-Encoder. Die main-Funktion basiert auf der Hilfsfunktion GetEncoderClsid, die unter Abrufen des Klassenbezeichners für einen [Encoder gezeigt wird.](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)


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



Wenn Sie die vorherige Konsolenanwendung ausführen, erhalten Sie eine Ausgabe ähnlich der folgenden:


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



Jedes [**encoderParameter-Objekt**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) im Array verfügt über die folgenden vier öffentlichen Datenmitglieder:

Der folgende Code ist eine Fortsetzung der Konsolenanwendung, die im vorherigen Beispiel gezeigt wird. Der Code untersucht das zweite [**EncoderParameter-Objekt**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) im Array, das von [**Image::GetEncoderParameterList zurückgegeben wird.**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) Der Code ruft [StringFromGUID2 auf.](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2)Dabei handelt es sich um eine in Objbase.h deklarierte Systemfunktion, um den **GUID-Member** des **EncoderParameter-Objekts** in eine Zeichenfolge zu konvertieren.


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



Sie können die GUID in Gdiplusimaging.h nachschlagen und feststellen, dass die Kategorie dieses [**EncoderParameter-Objekts**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) EncoderQuality ist. Sie können diese Kategorie (EncoderQuality) des Parameters verwenden, um die Komprimierungsstufe eines JPEG-Bilds zu festlegen.

In Gdiplusenums.h gibt die [**EncoderParameterValueType-Enumeration**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) an, dass der Datentyp 6 **ValueLongRange ist.** Ein langer Bereich ist ein Paar **von ULONG-Werten.**

Die Anzahl der Werte ist 1. Daher wissen wir, dass das **Value-Element** des [**EncoderParameter-Objekts**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) ein Zeiger auf ein Array mit einem Element ist. Dieses eine Element ist ein Paar von **ULONG-Werten.**

Der folgende Code ist eine Fortsetzung der Konsolenanwendung, die in den beiden vorherigen Beispielen gezeigt wird. Der Code definiert einen Datentyp namens **PLONGRANGE** (Zeiger auf einen langen Bereich). Eine Variable vom Typ **PLONGRANGE** wird verwendet, um die minimalen und maximalen Werte zu extrahieren, die als Qualitätseinstellung an den JPEG-Encoder übergeben werden können.


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



Im vorherigen Beispiel ist der im [**EncoderParameter-Objekt**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) zurückgegebene Wert ein Paar von **ULONG-Werten,** die die minimalen und maximalen möglichen Werte für den Qualitätsparameter angeben. In einigen Fällen sind die in einem **EncoderParameter-Objekt zurückgegebenen** Werte Member der [**EncoderValue-Enumeration.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) In den folgenden Themen werden die **EncoderValue-Enumeration** und Methoden zum Auflisten möglicher Parameterwerte ausführlicher erläutert:

-   [Verwenden der EncoderValue-Enumeration](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [Auflisten von Parametern und Werten für alle Encoder](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 
