---
description: Ein bestimmter Encoder unterstützt bestimmte Parameterkategorien, und für jede dieser Kategorien lässt dieser Encoder bestimmte Werte zu.
ms.assetid: cb9552e9-e807-4b07-b315-4550762e7026
title: Verwenden der EncoderValue-Enumeration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 488d465d27f7884ecc5999d38fea10afdac06b74b77d29338c8d0944a1261b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666320"
---
# <a name="using-the-encodervalue-enumeration"></a>Verwenden der EncoderValue-Enumeration

Ein bestimmter Encoder unterstützt bestimmte Parameterkategorien, und für jede dieser Kategorien lässt dieser Encoder bestimmte Werte zu. Beispielsweise unterstützt der JPEG-Encoder die EncoderValueQuality-Parameterkategorie, und die zulässigen Parameterwerte sind die ganzen Zahlen 0 bis 100. Einige der zulässigen Parameterwerte sind für mehrere Encoder identisch. Diese Standardwerte werden in der [**EncoderValue-Enumeration**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) in Gdiplusenums.h definiert:


```
enum EncoderValue
{
   EncoderValueColorTypeCMYK,             // 0
   EncoderValueColorTypeYCCK,             // 1
   EncoderValueCompressionLZW,            // 2
   EncoderValueCompressionCCITT3,         // 3
   EncoderValueCompressionCCITT4,         // 4
   EncoderValueCompressionRle,            // 5
   EncoderValueCompressionNone,           // 6
   EncoderValueScanMethodInterlaced,      // 7
   EncoderValueScanMethodNonInterlaced,   // 8
   EncoderValueVersionGif87,              // 9
   EncoderValueVersionGif89,              // 10
   EncoderValueRenderProgressive,         // 11
   EncoderValueRenderNonProgressive,      // 12
   EncoderValueTransformRotate90,         // 13
   EncoderValueTransformRotate180,        // 14
   EncoderValueTransformRotate270,        // 15
   EncoderValueTransformFlipHorizontal,   // 16
   EncoderValueTransformFlipVertical,     // 17
   EncoderValueMultiFrame,                // 18
   EncoderValueLastFrame,                 // 19
   EncoderValueFlush,                     // 20
   EncoderValueFrameDimensionTime,        // 21
   EncoderValueFrameDimensionResolution,  // 22
   EncoderValueFrameDimensionPage         // 23
};
```



Eine der vom JPEG-Encoder unterstützten Parameterkategorien ist die Kategorie EncoderTransformation. Wenn Sie die [**EncoderValue-Enumeration**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) untersuchen, könnten Sie spekulieren (und sie würden richtig sein), dass die Kategorie EncoderTransformation die folgenden fünf Werte zulässt:


```
EncoderValueTransformRotate90,          // 13
EncoderValueTransformRotate180,         // 14
EncoderValueTransformRotate270,         // 15
EncoderValueTransformFlipHorizontal,    // 16
EncoderValueTransformFlipVertical,      // 17
```



Die folgende Konsolenanwendung überprüft, ob der JPEG-Encoder die EncoderTransformation-Parameterkategorie unterstützt und dass es fünf zulässige Werte für einen solchen Parameter gibt. Die main-Funktion basiert auf der Hilfsfunktion GetEncoderClsid, die unter Abrufen des Klassenbezeichners für einen [Encoder gezeigt wird.](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);
INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   // Create a Bitmap (inherited from Image) object so that we can call
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
   // Look at the first (index 0) EncoderParameter object in the array.
   printf("Parameter[0]\n");
   WCHAR strGuid[39];
   StringFromGUID2(pEncoderParameters->Parameter[0].Guid, strGuid, 39);
   wprintf(L"   The guid is %s.\n", strGuid);
   printf("   The data type is %d.\n", 
      pEncoderParameters->Parameter[0].Type);
   printf("   The number of values is %d.\n",
      pEncoderParameters->Parameter[0].NumberOfValues);
   free(pEncoderParameters);
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Wenn Sie die vorherige Konsolenanwendung ausführen, erhalten Sie eine Ausgabe ähnlich der folgenden:


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
Parameter[0]
   The GUID is {8D0EB2D1-A58E-4EA8-AA14-108074B7B6F9}.
   The value type is 4.
   The number of values is 5.
```



Sie können die GUID in Gdiplusimaging.h nachschlagen und feststellen, dass die Kategorie dieses [**EncoderParameter-Objekts**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) EncoderTransformation ist. In Gdiplusenums.h gibt die [**EncoderParameterValueType-Enumeration**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) an, dass der Datentyp 4 ValueLong (32-Bit-Ganzzahl ohne Vorzeichen) ist. Die Anzahl der Werte ist fünf, daher wissen wir, dass das **Value-Member** des **EncoderParameter-Objekts** ein Zeiger auf ein Array von fünf **ULONG-Werten** ist.

Der folgende Code ist eine Fortsetzung der Konsolenanwendung, die im vorherigen Beispiel gezeigt wird. Der Code listet die zulässigen Werte für einen EncoderTransformation-Parameter auf:


```
ULONG* pUlong = (ULONG*)(pEncoderParameters->Parameter[0].Value);
ULONG numVals = pEncoderParameters->Parameter[0].NumberOfValues;
printf("%s", "   The allowable values are");
for(ULONG j = 0; j < numVals; ++j)
{
   printf("  %d", pUlong[j]);
}
```



Der oben genannte Code erzeugt die folgende Ausgabe:


```
The allowable values are  13  14  15  16  17
```



Die zulässigen Werte (13, 14, 15, 16 und 17) entsprechen den folgenden Membern der [**EncoderValue-Enumeration:**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue)


```
EncoderValueTransformRotate90,        // 13
EncoderValueTransformRotate180,       // 14
EncoderValueTransformRotate270,       // 15
EncoderValueTransformFlipHorizontal,  // 16
EncoderValueTransformFlipVertical,    // 17
```



 

 
