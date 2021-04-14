---
title: DVD. Back-Methode
description: Die Methode "Back" gibt die Anzeige von einem Untermenü an das übergeordnete Menü zurück.
ms.assetid: 4b6c3562-6484-4ef0-8c5c-c24d88e02096
keywords:
- Windows-Media Player der Back-Methode
- Back-Methode, Windows Media Player, DVD-Klasse
- DVD-Klasse, Windows Media Player, Back-Methode
topic_type:
- apiref
api_name:
- DVD.back
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e656051d02ec5efc74aa7595d2ca6cb20e648f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391916"
---
# <a name="dvdback-method"></a><span data-ttu-id="e6f9c-106">DVD. Back-Methode</span><span class="sxs-lookup"><span data-stu-id="e6f9c-106">DVD.back method</span></span>

<span data-ttu-id="e6f9c-107">Die Methode " **Back** " gibt die Anzeige von einem Untermenü an das übergeordnete Menü zurück.</span><span class="sxs-lookup"><span data-stu-id="e6f9c-107">The **back** method returns the display from a submenu to its parent menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6f9c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6f9c-108">Syntax</span></span>


```JScript
DVD.back()
```



## <a name="parameters"></a><span data-ttu-id="e6f9c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6f9c-109">Parameters</span></span>

<span data-ttu-id="e6f9c-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e6f9c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6f9c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6f9c-111">Return value</span></span>

<span data-ttu-id="e6f9c-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e6f9c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6f9c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6f9c-113">Remarks</span></span>

<span data-ttu-id="e6f9c-114">Jede DVD wird unterschiedlich verfasst.</span><span class="sxs-lookup"><span data-stu-id="e6f9c-114">Every DVD is authored differently.</span></span> <span data-ttu-id="e6f9c-115">Einige DVDs werden so erstellt, dass die **Back** -Methode über das Root-Menü verfügbar ist, aber wenn Sie aufgerufen wird, wird keine Aktion durchführen.</span><span class="sxs-lookup"><span data-stu-id="e6f9c-115">Some DVDs are authored so that the **back** method is available from the root menu, but when invoked, it will do nothing.</span></span>

<span data-ttu-id="e6f9c-116">**Windows Media Player 10 Mobile:** Diese Methode ist immer erfolgreich, führt jedoch nicht den beabsichtigten Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="e6f9c-116">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6f9c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6f9c-117">Requirements</span></span>



| <span data-ttu-id="e6f9c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6f9c-118">Requirement</span></span> | <span data-ttu-id="e6f9c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e6f9c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f9c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6f9c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e6f9c-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6f9c-121">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6f9c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6f9c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e6f9c-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6f9c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e6f9c-124">Version</span><span class="sxs-lookup"><span data-stu-id="e6f9c-124">Version</span></span><br/>                  | <span data-ttu-id="e6f9c-125">Windows Media Player für Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="e6f9c-125">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="e6f9c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e6f9c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6f9c-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6f9c-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6f9c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6f9c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6f9c-129">**DVD-Objekt**</span><span class="sxs-lookup"><span data-stu-id="e6f9c-129">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





