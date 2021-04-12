---
title: CCM_GETVERSION Meldung (kommstrg. h)
description: Ruft die Versionsnummer für ein Steuerelement ab, das von der aktuellen ccm-setVersion-Nachricht festgelegt wird \_ .
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- Windows-Steuerelemente für CCM_GETVERSION Meldung
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd302774f8821b51a4abaf72bccc403e7302e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104511"
---
# <a name="ccm_getversion-message"></a><span data-ttu-id="df13b-104">CCM- \_ GetVersion-Meldung</span><span class="sxs-lookup"><span data-stu-id="df13b-104">CCM\_GETVERSION message</span></span>

<span data-ttu-id="df13b-105">Ruft die Versionsnummer für ein Steuerelement ab, das von der aktuellen [**ccm- \_ setVersion**](ccm-setversion.md) -Nachricht festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="df13b-105">Gets the version number for a control set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="df13b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="df13b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df13b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df13b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="df13b-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="df13b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="df13b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df13b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="df13b-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="df13b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df13b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df13b-111">Return value</span></span>

<span data-ttu-id="df13b-112">Gibt die Versionsnummer zurück, die von der aktuellen [**ccm- \_ setVersion**](ccm-setversion.md) -Nachricht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="df13b-112">Returns the version number set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="df13b-113">Wenn eine solche Nachricht nicht gesendet wurde, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="df13b-113">If no such message has been sent, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="df13b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df13b-114">Remarks</span></span>

<span data-ttu-id="df13b-115">Diese Meldung gibt die dll-Version nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="df13b-115">This message does not return the DLL version.</span></span> <span data-ttu-id="df13b-116">Eine Erläuterung der Verwendung von [**dllgetversion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) zum Abrufen der aktuellen dll-Version finden Sie unter [Shell-Versionen](common-control-versions.md) .</span><span class="sxs-lookup"><span data-stu-id="df13b-116">See [Shell Versions](common-control-versions.md) for a discussion of how to use [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) to retrieve the current DLL version.</span></span>

> [!Note]  
> <span data-ttu-id="df13b-117">Die Versionsnummer wird für ein Steuerelement als Steuerelement festgelegt und ist möglicherweise nicht für alle Steuerelemente identisch.</span><span class="sxs-lookup"><span data-stu-id="df13b-117">The version number is set on a control by control basis, and may not be the same for all controls.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="df13b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df13b-118">Requirements</span></span>



| <span data-ttu-id="df13b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df13b-119">Requirement</span></span> | <span data-ttu-id="df13b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="df13b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df13b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df13b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="df13b-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df13b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df13b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df13b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="df13b-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df13b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df13b-125">Header</span><span class="sxs-lookup"><span data-stu-id="df13b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="df13b-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="df13b-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

