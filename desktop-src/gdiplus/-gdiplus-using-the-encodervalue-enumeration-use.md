---
description: Ein bestimmter Encoder unterstützt bestimmte Parameter Kategorien. für jede dieser Kategorien lässt dieser Encoder bestimmte Werte zu.
ms.assetid: cb9552e9-e807-4b07-b315-4550762e7026
title: Verwenden der EncoderValue-Enumeration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d755248150e81f963ea1c5c597ab04649c342944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978904"
---
# <a name="using-the-encodervalue-enumeration"></a>Verwenden der EncoderValue-Enumeration

Ein bestimmter Encoder unterstützt bestimmte Parameter Kategorien. für jede dieser Kategorien lässt dieser Encoder bestimmte Werte zu. Der JPEG-Encoder unterstützt z. b. die encodervaluequality-Parameter Kategorie, und die zulässigen Parameterwerte sind die ganzen Zahlen 0 bis 100. Einige der zulässigen Parameterwerte sind in mehreren Encodern gleich. Diese Standardwerte werden in der [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) -Enumeration in "gdiplusenums. h" definiert:


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



Eine der vom JPEG-Encoder unterstützten Parameter Kategorien ist die encodertransformation-Kategorie. Wenn Sie die [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) -Enumeration untersuchen, können Sie vermuten (und Sie sind korrekt), dass die encodertransformation-Kategorie die folgenden fünf Werte zulässt:


```
EncoderValueTransformRotate90,          // 13
EncoderValueTransformRotate180,         // 14
EncoderValueTransformRotate270,         // 15
EncoderValueTransformFlipHorizontal,    // 16
EncoderValueTransformFlipVertical,      // 17
```



Die folgende Konsolenanwendung überprüft, ob der JPEG-Encoder die encodertransformation-Parameter Kategorie unterstützt und dass es fünf zulässige Werte für einen solchen Parameter gibt. Die Main-Funktion basiert auf der-Hilfsfunktion getencoderclsid, die unter [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)angezeigt wird.


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



Wenn Sie die vorherige Konsolenanwendung ausführen, erhalten Sie eine Ausgabe wie die folgende:


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
Parameter[0]
   The GUID is {8D0EB2D1-A58E-4EA8-AA14-108074B7B6F9}.
   The value type is 4.
   The number of values is 5.
```



Sie können die GUID in "gdiplusimaging. h" nachschlagen und herausfinden, dass die Kategorie dieses [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekts "encodertransformation" lautet. In "gdiplusenums. h" gibt die [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) -Enumeration an, dass der Datentyp 4 valuelong (32-Bit-Ganzzahl ohne Vorzeichen) ist. Die Anzahl der Werte beträgt fünf. daher wissen wir, dass der **Wertmember** des **EncoderParameter** -Objekts ein Zeiger auf ein Array mit fünf **ulong** -Werten ist.

Der folgende Code ist eine Fortsetzung der Konsolenanwendung, die im vorherigen Beispiel gezeigt wird. Der Code listet die zulässigen Werte für einen encodertransformation-Parameter auf:


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



Die zulässigen Werte (13, 14, 15, 16 und 17) entsprechen den folgenden Membern der [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) -Enumeration:


```
EncoderValueTransformRotate90,        // 13
EncoderValueTransformRotate180,       // 14
EncoderValueTransformRotate270,       // 15
EncoderValueTransformFlipHorizontal,  // 16
EncoderValueTransformFlipVertical,    // 17
```



 

 
