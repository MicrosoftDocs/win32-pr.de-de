---
description: Gibt an, ob der angegebene nicht-Farbstil unterstrichen ist.
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: Idulimestyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372186"
---
# <a name="idulimestyle-function"></a><span data-ttu-id="ceb3e-103">Idulimestyle-Funktion</span><span class="sxs-lookup"><span data-stu-id="ceb3e-103">IdUlIMEStyle function</span></span>

<span data-ttu-id="ceb3e-104">Gibt an, ob der angegebene nicht-Farbstil unterstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="ceb3e-104">Identifies whether the specified non-color style has underline.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceb3e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ceb3e-105">Syntax</span></span>


```C++
UINT __cdecl IdUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="ceb3e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ceb3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceb3e-107">*pimestyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ceb3e-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceb3e-108">Eine **imestyle** -Struktur, die von der [**pimestylefromattr**](pimestylefromattr.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ceb3e-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceb3e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ceb3e-109">Return value</span></span>

<span data-ttu-id="ceb3e-110">Diese Funktion kann einen der folgenden Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ceb3e-110">This function can returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ceb3e-111">**Imesty \_ UL \_ Min** . (2002)</span><span class="sxs-lookup"><span data-stu-id="ceb3e-111">**IMESTY\_UL\_MIN** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="ceb3e-112">**Imesty \_ UL \_ None** (2002)</span><span class="sxs-lookup"><span data-stu-id="ceb3e-112">**IMESTY\_UL\_NONE** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="ceb3e-113">**Imesty \_ UL ( \_ einzeln** ) (2003)</span><span class="sxs-lookup"><span data-stu-id="ceb3e-113">**IMESTY\_UL\_SINGLE** (2003)</span></span>
</dt> <dt>

<span data-ttu-id="ceb3e-114">**Imesty \_ UL- \_ gepunktete** (2005)</span><span class="sxs-lookup"><span data-stu-id="ceb3e-114">**IMESTY\_UL\_DOTTED** (2005)</span></span>
</dt> <dt>

<span data-ttu-id="ceb3e-115">**Imesty \_ UL \_ Thick** (2006)</span><span class="sxs-lookup"><span data-stu-id="ceb3e-115">**IMESTY\_UL\_THICK** (2006)</span></span>
</dt> <dt>

<span data-ttu-id="ceb3e-116">**Imesty \_ UL \_ niedriger** (2011)</span><span class="sxs-lookup"><span data-stu-id="ceb3e-116">**IMESTY\_UL\_LOWER** (2011)</span></span>
</dt> <dt>

<span data-ttu-id="ceb3e-117">**Imesty \_ UL Thick \_ Lower** (2012)</span><span class="sxs-lookup"><span data-stu-id="ceb3e-117">**IMESTY\_UL\_THICKLOWER** (2012)</span></span>
</dt> <dt>

<span data-ttu-id="ceb3e-118">**Imesty \_ UL \_ thickdithlower** (2013)</span><span class="sxs-lookup"><span data-stu-id="ceb3e-118">**IMESTY\_UL\_THICKDITHLOWER** (2013)</span></span>
</dt> <dt>

<span data-ttu-id="ceb3e-119">**Imesty \_ UL \_ dithlower** (2014)</span><span class="sxs-lookup"><span data-stu-id="ceb3e-119">**IMESTY\_UL\_DITHLOWER** (2014)</span></span>
</dt> <dt>

<span data-ttu-id="ceb3e-120">**Imesty \_ \_Max. UL** (2014)</span><span class="sxs-lookup"><span data-stu-id="ceb3e-120">**IMESTY\_UL\_MAX** (2014)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ceb3e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ceb3e-121">Remarks</span></span>

<span data-ttu-id="ceb3e-122">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ceb3e-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceb3e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ceb3e-123">Requirements</span></span>



| <span data-ttu-id="ceb3e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ceb3e-124">Requirement</span></span> | <span data-ttu-id="ceb3e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ceb3e-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb3e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ceb3e-126">DLL</span></span><br/> | <dl> <span data-ttu-id="ceb3e-127"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ceb3e-127"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceb3e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ceb3e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb3e-129">**Pimestylefromattr**</span><span class="sxs-lookup"><span data-stu-id="ceb3e-129">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
