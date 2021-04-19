---
description: Die widestringfromresource-Funktion lädt eine breit Zeichen-Zeichenfolge aus einer Ressourcen Datei mit dem angegebenen Ressourcen Bezeichner.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: Widestringfromresource-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c7cbdccc76fc57e660109851ae5b8f141704d04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368587"
---
# <a name="widestringfromresource-function"></a><span data-ttu-id="b0d08-103">Widestringfromresource-Funktion</span><span class="sxs-lookup"><span data-stu-id="b0d08-103">WideStringFromResource function</span></span>

<span data-ttu-id="b0d08-104">Die- `WideStringFromResource` Funktion lädt eine breit Zeichen-Zeichenfolge aus einer Ressourcen Datei mit dem angegebenen Ressourcen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b0d08-104">The `WideStringFromResource` function loads a wide-character string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0d08-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0d08-105">Syntax</span></span>


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="b0d08-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0d08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0d08-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="b0d08-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="b0d08-108">Ein Zeiger auf die Zeichenfolge, die " *iResourceID*" entspricht.</span><span class="sxs-lookup"><span data-stu-id="b0d08-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="b0d08-109">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="b0d08-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="b0d08-110">Der Ressourcen Bezeichner der abzurufenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b0d08-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0d08-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0d08-111">Return value</span></span>

<span data-ttu-id="b0d08-112">Gibt die gleiche Zeichenfolge wie *pbuffer* zurück.</span><span class="sxs-lookup"><span data-stu-id="b0d08-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="b0d08-113">Wenn die Funktion nicht erfolgreich ist, wird eine NULL-Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b0d08-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0d08-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0d08-114">Remarks</span></span>

<span data-ttu-id="b0d08-115">Eigenschaften Seiten werden in der Regel über Ihre COM-Schnittstellen aufgerufen, die Zeichen folgen mit breit Zeichen verwenden, unabhängig davon, wie die Binärdatei erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b0d08-115">Property pages are typically called through their COM interfaces, which use wide-character strings regardless of how the binary is built.</span></span> <span data-ttu-id="b0d08-116">Diese Funktion ermöglicht es Ihnen, eine Ressourcen Zeichenfolge in eine Zeichenfolge mit breit Zeichen zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="b0d08-116">This function allows you to convert a resource string to a wide-character string.</span></span> <span data-ttu-id="b0d08-117">Die-Funktion konvertiert die Ressource nach dem Laden in eine Zeichenfolge mit breit Zeichen (wenn Sie noch nicht vorhanden ist).</span><span class="sxs-lookup"><span data-stu-id="b0d08-117">The function converts the resource to a wide-character string (if it is not already one) after loading it.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0d08-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0d08-118">Requirements</span></span>



| <span data-ttu-id="b0d08-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0d08-119">Requirement</span></span> | <span data-ttu-id="b0d08-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b0d08-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d08-121">Header</span><span class="sxs-lookup"><span data-stu-id="b0d08-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b0d08-122"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0d08-122"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b0d08-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b0d08-123">Library</span></span><br/> | <dl> <span data-ttu-id="b0d08-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b0d08-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0d08-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0d08-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0d08-126">Hilfsfunktionen für Eigenschaften Seiten</span><span class="sxs-lookup"><span data-stu-id="b0d08-126">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




