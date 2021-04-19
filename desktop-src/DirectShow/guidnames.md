---
description: Guidnames ist ein globales Array in der DirectShow-Basisklassen Bibliothek, das Zeichen folgen enthält, die die in UUIDs. h definierten GUIDs darstellen. Dieses Array ist hilfreich beim Erzeugen der Debugausgabe.
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: Guidnames (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GuidNames
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359294d0cf3ab4e2074db5935cbbd604dcc1b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358089"
---
# <a name="guidnames"></a><span data-ttu-id="f097d-104">Guidnames</span><span class="sxs-lookup"><span data-stu-id="f097d-104">GuidNames</span></span>

<span data-ttu-id="f097d-105">`GuidNames` bei handelt es sich um ein globales Array in der DirectShow-Basisklassen Bibliothek, das Zeichen folgen enthält, die die in UUIDs. h definierten GUIDs darstellen.</span><span class="sxs-lookup"><span data-stu-id="f097d-105">`GuidNames` is a global array in the DirectShow base class library that contains strings representing the GUIDs defined in Uuids.h.</span></span> <span data-ttu-id="f097d-106">Dieses Array ist hilfreich beim Erzeugen der Debugausgabe.</span><span class="sxs-lookup"><span data-stu-id="f097d-106">This array is useful for generating debug output.</span></span>

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a><span data-ttu-id="f097d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f097d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f097d-108"><span id="guid"></span><span id="GUID"></span>*GUID*</span><span class="sxs-lookup"><span data-stu-id="f097d-108"><span id="guid"></span><span id="GUID"></span>*guid*</span></span>
</dt> <dd>

<span data-ttu-id="f097d-109">Gibt jeden GUID-Wert an, der in der Header Datei "UUIDs. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f097d-109">Specifies any GUID value defined in the header file Uuids.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f097d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f097d-110">Remarks</span></span>

<span data-ttu-id="f097d-111">Verwenden Sie dieses globale Array, um GUID-Konstanten als Zeichen folgen auszugeben.</span><span class="sxs-lookup"><span data-stu-id="f097d-111">Use this global array to output GUID constants as strings.</span></span> <span data-ttu-id="f097d-112">Der folgende Code gibt z. b. die Zeichenfolge "MediaType \_ Video" in der Konsole aus:</span><span class="sxs-lookup"><span data-stu-id="f097d-112">For example, the following code prints the string "MEDIATYPE\_Video" to the console:</span></span>


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



<span data-ttu-id="f097d-113">Wenn die GUID nicht übereinstimmt, wird die Zeichenfolge "Unbekannter GUID-Name" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f097d-113">If the GUID is not matched, the string "Unknown GUID Name" is returned.</span></span> <span data-ttu-id="f097d-114">Nicht alle DirectShow-GUIDs sind in "UUIDs. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="f097d-114">Not all DirectShow GUIDs are defined in uuids.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="f097d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f097d-115">Requirements</span></span>



| <span data-ttu-id="f097d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f097d-116">Requirement</span></span> | <span data-ttu-id="f097d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f097d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f097d-118">Header</span><span class="sxs-lookup"><span data-stu-id="f097d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f097d-119"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f097d-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f097d-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f097d-120">Library</span></span><br/> | <dl> <span data-ttu-id="f097d-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f097d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f097d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f097d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f097d-123">Debug-Ausgabefunktionen</span><span class="sxs-lookup"><span data-stu-id="f097d-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




