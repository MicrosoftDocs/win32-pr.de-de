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
# <a name="determining-the-parameters-supported-by-an-encoder"></a><span data-ttu-id="befe3-103">Bestimmen der von einem Encoder unterstützten Parameter</span><span class="sxs-lookup"><span data-stu-id="befe3-103">Determining the Parameters Supported by an Encoder</span></span>

<span data-ttu-id="befe3-104">Die [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse stellt die [**Image:: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) -Methode bereit, sodass Sie die Parameter ermitteln können, die von einem bestimmten Bild Encoder unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="befe3-104">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides the [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) method so that you can determine the parameters that are supported by a given image encoder.</span></span> <span data-ttu-id="befe3-105">Die **Image:: GetEncoderParameterList** -Methode gibt ein Array von [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="befe3-105">The **Image::GetEncoderParameterList** method returns an array of [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects.</span></span> <span data-ttu-id="befe3-106">Vor dem Aufrufen von **Image:: GetEncoderParameterList** müssen Sie einen Puffer zuordnen, um das Array zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="befe3-106">You must allocate a buffer to receive that array before you call **Image::GetEncoderParameterList**.</span></span> <span data-ttu-id="befe3-107">Sie können " [**Image:: getencoderparameterlistsize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) " aufrufen, um die Größe des erforderlichen Puffers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="befe3-107">You can call [**Image::GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) to determine the size of the required buffer.</span></span>

<span data-ttu-id="befe3-108">Die folgende Konsolenanwendung ruft die Parameterliste für den JPEG-Encoder ab.</span><span class="sxs-lookup"><span data-stu-id="befe3-108">The following console application obtains the parameter list for the JPEG encoder.</span></span> <span data-ttu-id="befe3-109">Die Main-Funktion basiert auf der-Hilfsfunktion getencoderclsid, die unter [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="befe3-109">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



<span data-ttu-id="befe3-110">Wenn Sie die vorherige Konsolenanwendung ausführen, erhalten Sie eine Ausgabe wie die folgende:</span><span class="sxs-lookup"><span data-stu-id="befe3-110">When you run the preceding console application, you get an output similar to the following:</span></span>


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



<span data-ttu-id="befe3-111">Jedes der [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekte im Array verfügt über die folgenden vier öffentlichen Datenmember:</span><span class="sxs-lookup"><span data-stu-id="befe3-111">Each of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects in the array has the following four public data members:</span></span>

<span data-ttu-id="befe3-112">Der folgende Code ist eine Fortsetzung der Konsolenanwendung, die im vorherigen Beispiel gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="befe3-112">The following code is a continuation of the console application shown in the preceding example.</span></span> <span data-ttu-id="befe3-113">Der Code untersucht das zweite [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekt im Array, das von [**Image:: GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="befe3-113">The code looks at the second [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object in the array returned by [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist).</span></span> <span data-ttu-id="befe3-114">Der Code ruft [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2)auf, bei dem es sich um eine Systemfunktion handelt, die in objbase. h deklariert ist, um den **GUID** -Member des **EncoderParameter** -Objekts in eine Zeichenfolge zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="befe3-114">The code calls [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), which is a system function declared in Objbase.h, to convert the **Guid** member of the **EncoderParameter** object to a string.</span></span>


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



<span data-ttu-id="befe3-115">Der oben genannte Code erzeugt die folgende Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="befe3-115">The preceding code produces the following output:</span></span>


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



<span data-ttu-id="befe3-116">Sie können die GUID in "gdiplusimaging. h" nachschlagen und herausfinden, dass die Kategorie dieses [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekts "encoderquality" ist.</span><span class="sxs-lookup"><span data-stu-id="befe3-116">You can look up the GUID in Gdiplusimaging.h and find out that the category of this [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is EncoderQuality.</span></span> <span data-ttu-id="befe3-117">Sie können diese Kategorie (encoderquality) des Parameters verwenden, um die Komprimierungs Ebene eines JPEG-Bilds festzulegen.</span><span class="sxs-lookup"><span data-stu-id="befe3-117">You can use this category (EncoderQuality) of parameter to set the compression level of a JPEG image.</span></span>

<span data-ttu-id="befe3-118">In gdiplusenums. h gibt die [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) -Enumeration an, dass der Datentyp 6 **valuelongrange** ist.</span><span class="sxs-lookup"><span data-stu-id="befe3-118">In Gdiplusenums.h, the [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) enumeration indicates that data type 6 is **ValueLongRange**.</span></span> <span data-ttu-id="befe3-119">Ein langer Bereich ist ein paar von **ulong** -Werten.</span><span class="sxs-lookup"><span data-stu-id="befe3-119">A long range is a pair of **ULONG** values.</span></span>

<span data-ttu-id="befe3-120">Die Anzahl der Werte ist 1. daher wissen wir, dass der **Wertmember** des [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekts ein Zeiger auf ein Array mit einem Element ist.</span><span class="sxs-lookup"><span data-stu-id="befe3-120">The number of values is one, so we know that the **Value** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pointer to an array that has one element.</span></span> <span data-ttu-id="befe3-121">Ein Element ist ein paar von **ulong** -Werten.</span><span class="sxs-lookup"><span data-stu-id="befe3-121">That one element is a pair of **ULONG** values.</span></span>

<span data-ttu-id="befe3-122">Der folgende Code ist eine Fortsetzung der Konsolenanwendung, die in den vorherigen beiden Beispielen gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="befe3-122">The following code is a continuation of the console application that is shown in the preceding two examples.</span></span> <span data-ttu-id="befe3-123">Der Code definiert einen Datentyp namens **plongrange** (Zeiger auf einen langen Bereich).</span><span class="sxs-lookup"><span data-stu-id="befe3-123">The code defines a data type called **PLONGRANGE** (pointer to a long range).</span></span> <span data-ttu-id="befe3-124">Eine Variable vom Typ **plongrange** wird verwendet, um die Mindest-und Höchstwerte zu extrahieren, die als Qualitätseinstellung an den JPEG-Encoder übermittelt werden können.</span><span class="sxs-lookup"><span data-stu-id="befe3-124">A variable of type **PLONGRANGE** is used to extract the minimum and maximum values that can be passed as a quality setting to the JPEG encoder.</span></span>


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



<span data-ttu-id="befe3-125">Der oben genannte Code erzeugt die folgende Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="befe3-125">The preceding code produces the following output:</span></span>


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



<span data-ttu-id="befe3-126">Im vorherigen Beispiel ist der Wert, der im [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekt zurückgegeben wird, ein paar von **ulong** -Werten, die die minimalen und maximalen möglichen Werte für den Quality-Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="befe3-126">In the preceding example, the value returned in the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pair of **ULONG** values that indicate the minimum and maximum possible values for the quality parameter.</span></span> <span data-ttu-id="befe3-127">In einigen Fällen sind die Werte, die in einem **EncoderParameter** -Objekt zurückgegeben werden, Member der [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="befe3-127">In some cases, the values returned in an **EncoderParameter** object are members of the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration.</span></span> <span data-ttu-id="befe3-128">In den folgenden Themen werden die **EncoderValue** -Enumeration und Methoden zum Auflisten möglicher Parameterwerte ausführlicher erläutert:</span><span class="sxs-lookup"><span data-stu-id="befe3-128">The following topics discuss the **EncoderValue** enumeration and methods for listing possible parameter values in more detail:</span></span>

-   [<span data-ttu-id="befe3-129">Verwenden der EncoderValue-Enumeration</span><span class="sxs-lookup"><span data-stu-id="befe3-129">Using the EncoderValue Enumeration</span></span>](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [<span data-ttu-id="befe3-130">Auflisten von Parametern und Werten für alle Encoder</span><span class="sxs-lookup"><span data-stu-id="befe3-130">Listing Parameters and Values for All Encoders</span></span>](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 
