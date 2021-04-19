---
description: Die stringfromresource-Funktion lädt eine Zeichenfolge aus einer Ressourcen Datei mit dem angegebenen Ressourcen Bezeichner.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: Stringfromresource-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371723"
---
# <a name="stringfromresource-function"></a><span data-ttu-id="96c74-103">Stringfromresource-Funktion</span><span class="sxs-lookup"><span data-stu-id="96c74-103">StringFromResource function</span></span>

<span data-ttu-id="96c74-104">Die- `StringFromResource` Funktion lädt eine Zeichenfolge aus einer Ressourcen Datei mit dem angegebenen Ressourcen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="96c74-104">The `StringFromResource` function loads a string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96c74-105">Syntax</span></span>


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="96c74-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="96c74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96c74-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="96c74-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="96c74-108">Ein Zeiger auf die Zeichenfolge, die " *iResourceID*" entspricht.</span><span class="sxs-lookup"><span data-stu-id="96c74-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="96c74-109">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="96c74-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="96c74-110">Der Ressourcen Bezeichner der abzurufenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="96c74-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96c74-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96c74-111">Return value</span></span>

<span data-ttu-id="96c74-112">Gibt die gleiche Zeichenfolge wie *pbuffer* zurück.</span><span class="sxs-lookup"><span data-stu-id="96c74-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="96c74-113">Wenn die Funktion nicht erfolgreich ist, wird eine NULL-Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="96c74-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="96c74-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96c74-114">Remarks</span></span>

<span data-ttu-id="96c74-115">Der *pbuffer* -Puffer muss mindestens Str \_ Maximale \_ Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="96c74-115">The *pBuffer* buffer must be at least STR\_MAX\_LENGTH bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="96c74-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96c74-116">Requirements</span></span>



| <span data-ttu-id="96c74-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96c74-117">Requirement</span></span> | <span data-ttu-id="96c74-118">Wert</span><span class="sxs-lookup"><span data-stu-id="96c74-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96c74-119">Header</span><span class="sxs-lookup"><span data-stu-id="96c74-119">Header</span></span><br/>  | <dl> <span data-ttu-id="96c74-120"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96c74-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="96c74-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="96c74-121">Library</span></span><br/> | <dl> <span data-ttu-id="96c74-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="96c74-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96c74-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96c74-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c74-124">Hilfsfunktionen für Eigenschaften Seiten</span><span class="sxs-lookup"><span data-stu-id="96c74-124">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




