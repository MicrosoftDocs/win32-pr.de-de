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
# <a name="using-the-encodervalue-enumeration"></a><span data-ttu-id="6a1f1-103">Verwenden der EncoderValue-Enumeration</span><span class="sxs-lookup"><span data-stu-id="6a1f1-103">Using the EncoderValue Enumeration</span></span>

<span data-ttu-id="6a1f1-104">Ein bestimmter Encoder unterstützt bestimmte Parameter Kategorien. für jede dieser Kategorien lässt dieser Encoder bestimmte Werte zu.</span><span class="sxs-lookup"><span data-stu-id="6a1f1-104">A given encoder supports certain parameter categories, and for each of those categories, that encoder allows certain values.</span></span> <span data-ttu-id="6a1f1-105">Der JPEG-Encoder unterstützt z. b. die encodervaluequality-Parameter Kategorie, und die zulässigen Parameterwerte sind die ganzen Zahlen 0 bis 100.</span><span class="sxs-lookup"><span data-stu-id="6a1f1-105">For example, the JPEG encoder supports the EncoderValueQuality parameter category, and the allowable parameter values are the integers 0 through 100.</span></span> <span data-ttu-id="6a1f1-106">Einige der zulässigen Parameterwerte sind in mehreren Encodern gleich.</span><span class="sxs-lookup"><span data-stu-id="6a1f1-106">Some of the allowable parameter values are the same across several encoders.</span></span> <span data-ttu-id="6a1f1-107">Diese Standardwerte werden in der [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) -Enumeration in "gdiplusenums. h" definiert:</span><span class="sxs-lookup"><span data-stu-id="6a1f1-107">These standard values are defined in the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration in Gdiplusenums.h:</span></span>


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



<span data-ttu-id="6a1f1-108">Eine der vom JPEG-Encoder unterstützten Parameter Kategorien ist die encodertransformation-Kategorie.</span><span class="sxs-lookup"><span data-stu-id="6a1f1-108">One of the parameter categories supported by the JPEG encoder is the EncoderTransformation category.</span></span> <span data-ttu-id="6a1f1-109">Wenn Sie die [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) -Enumeration untersuchen, können Sie vermuten (und Sie sind korrekt), dass die encodertransformation-Kategorie die folgenden fünf Werte zulässt:</span><span class="sxs-lookup"><span data-stu-id="6a1f1-109">By examining the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration, you might speculate (and you would be correct) that the EncoderTransformation category allows the following five values:</span></span>


```
EncoderValueTransformRotate90,          // 13
EncoderValueTransformRotate180,         // 14
EncoderValueTransformRotate270,         // 15
EncoderValueTransformFlipHorizontal,    // 16
EncoderValueTransformFlipVertical,      // 17
```



<span data-ttu-id="6a1f1-110">Die folgende Konsolenanwendung überprüft, ob der JPEG-Encoder die encodertransformation-Parameter Kategorie unterstützt und dass es fünf zulässige Werte für einen solchen Parameter gibt.</span><span class="sxs-lookup"><span data-stu-id="6a1f1-110">The following console application verifies that the JPEG encoder supports the EncoderTransformation parameter category and that there are five allowable values for such a parameter.</span></span> <span data-ttu-id="6a1f1-111">Die Main-Funktion basiert auf der-Hilfsfunktion getencoderclsid, die unter [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6a1f1-111">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



<span data-ttu-id="6a1f1-112">Wenn Sie die vorherige Konsolenanwendung ausführen, erhalten Sie eine Ausgabe wie die folgende:</span><span class="sxs-lookup"><span data-stu-id="6a1f1-112">When you run the preceding console application, you get an output similar to the following:</span></span>


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
Parameter[0]
   The GUID is {8D0EB2D1-A58E-4EA8-AA14-108074B7B6F9}.
   The value type is 4.
   The number of values is 5.
```



<span data-ttu-id="6a1f1-113">Sie können die GUID in "gdiplusimaging. h" nachschlagen und herausfinden, dass die Kategorie dieses [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekts "encodertransformation" lautet.</span><span class="sxs-lookup"><span data-stu-id="6a1f1-113">You can look up the GUID in Gdiplusimaging.h and find out that the category of this [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is EncoderTransformation.</span></span> <span data-ttu-id="6a1f1-114">In "gdiplusenums. h" gibt die [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) -Enumeration an, dass der Datentyp 4 valuelong (32-Bit-Ganzzahl ohne Vorzeichen) ist.</span><span class="sxs-lookup"><span data-stu-id="6a1f1-114">In Gdiplusenums.h, the [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) enumeration indicates that data type 4 is ValueLong (32-bit unsigned integer).</span></span> <span data-ttu-id="6a1f1-115">Die Anzahl der Werte beträgt fünf. daher wissen wir, dass der **Wertmember** des **EncoderParameter** -Objekts ein Zeiger auf ein Array mit fünf **ulong** -Werten ist.</span><span class="sxs-lookup"><span data-stu-id="6a1f1-115">The number of values is five, so we know that the **Value** member of the **EncoderParameter** object is a pointer to an array of five **ULONG** values.</span></span>

<span data-ttu-id="6a1f1-116">Der folgende Code ist eine Fortsetzung der Konsolenanwendung, die im vorherigen Beispiel gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6a1f1-116">The following code is a continuation of the console application that is shown in the preceding example.</span></span> <span data-ttu-id="6a1f1-117">Der Code listet die zulässigen Werte für einen encodertransformation-Parameter auf:</span><span class="sxs-lookup"><span data-stu-id="6a1f1-117">The code lists the allowable values for an EncoderTransformation parameter:</span></span>


```
ULONG* pUlong = (ULONG*)(pEncoderParameters->Parameter[0].Value);
ULONG numVals = pEncoderParameters->Parameter[0].NumberOfValues;
printf("%s", "   The allowable values are");
for(ULONG j = 0; j < numVals; ++j)
{
   printf("  %d", pUlong[j]);
}
```



<span data-ttu-id="6a1f1-118">Der oben genannte Code erzeugt die folgende Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="6a1f1-118">The preceding code produces the following output:</span></span>


```
The allowable values are  13  14  15  16  17
```



<span data-ttu-id="6a1f1-119">Die zulässigen Werte (13, 14, 15, 16 und 17) entsprechen den folgenden Membern der [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) -Enumeration:</span><span class="sxs-lookup"><span data-stu-id="6a1f1-119">The allowable values (13, 14, 15, 16, and 17) correspond to the following members of the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration:</span></span>


```
EncoderValueTransformRotate90,        // 13
EncoderValueTransformRotate180,       // 14
EncoderValueTransformRotate270,       // 15
EncoderValueTransformFlipHorizontal,  // 16
EncoderValueTransformFlipVertical,    // 17
```



 

 
