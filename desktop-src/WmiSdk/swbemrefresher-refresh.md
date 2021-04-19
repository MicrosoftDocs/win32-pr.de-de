---
description: Die Methode "Swap. Refresh" aktualisiert alle Elemente, die im "Swap-Refresh Sher"-Objekt enthalten sind. Das Swap-Aktualisierungs Objekt.
ms.assetid: 85a4777a-4be7-44f2-b7a6-e18b5e57f7af
ms.tgt_platform: multiple
title: Methode ' Swap. Refresh ' (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Refresh
- ISWbemRefresher.Refresh
- ISWbemRefresher.Refresh
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8b2522227041858770c7256d7d2520cc661948e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106364284"
---
# <a name="swbemrefresherrefresh-method"></a><span data-ttu-id="d8871-103">Taubemrefresh Sher. Refresh-Methode</span><span class="sxs-lookup"><span data-stu-id="d8871-103">SWbemRefresher.Refresh method</span></span>

<span data-ttu-id="d8871-104">Die Methode " **Swap. Refresh** " aktualisiert alle Elemente, die im "Swap-Refresh [**Sher**](swbemrefresher.md) "-Objekt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d8871-104">The **SWbemRefresher.Refresh** method updates all the items that are contained in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="d8871-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d8871-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8871-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8871-106">Syntax</span></span>


```VB
SWbemRefresher.Refresh( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d8871-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8871-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8871-108">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="d8871-108">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d8871-109">Flags müssen auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d8871-109">Flags must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8871-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8871-110">Return value</span></span>

<span data-ttu-id="d8871-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d8871-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8871-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8871-112">Requirements</span></span>



| <span data-ttu-id="d8871-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8871-113">Requirement</span></span> | <span data-ttu-id="d8871-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d8871-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8871-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8871-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d8871-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8871-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8871-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8871-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d8871-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8871-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8871-119">Header</span><span class="sxs-lookup"><span data-stu-id="d8871-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8871-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8871-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8871-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d8871-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="d8871-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d8871-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d8871-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d8871-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8871-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8871-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d8871-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="d8871-125">CLSID</span></span><br/>                    | <span data-ttu-id="d8871-126">CLSID- \_ Austauschprogramm</span><span class="sxs-lookup"><span data-stu-id="d8871-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="d8871-127">IID</span><span class="sxs-lookup"><span data-stu-id="d8871-127">IID</span></span><br/>                      | <span data-ttu-id="d8871-128">IID \_ iswbemfreshsher</span><span class="sxs-lookup"><span data-stu-id="d8871-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="d8871-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8871-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8871-130">**Swap-Aktualisierungs Programm**</span><span class="sxs-lookup"><span data-stu-id="d8871-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




