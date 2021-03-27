---
description: Benachrichtigt eine appbar, dass sich der automatische Ausblenden der Taskleiste oder der Always on-Top-Status&8212 geändert hat, d \# . h., der Benutzer hat den &0034 ausgewählt oder gelöscht \# . Always on-&\# 0034; oder &\# 0034; Automatisches Ausblenden&\# 0034; Kontrollkästchen auf dem Eigenschaften Blatt der Taskleiste.
title: ABN_STATECHANGE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ac2c00a2-ac20-40a5-947e-6b75a2620a0b
api_name:
- ABN_STATECHANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 33879fcb5e9435e2245bc3d00a9fab75bf1cbdc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862135"
---
# <a name="abn_statechange-message"></a><span data-ttu-id="08464-103">ABN \_ StateChange-Nachricht</span><span class="sxs-lookup"><span data-stu-id="08464-103">ABN\_STATECHANGE message</span></span>

<span data-ttu-id="08464-104">Benachrichtigt eine appbar, dass sich der Zustand der Auto-oder Always on-Top-Taskleiste geändert hat, d. h., der Benutzer hat das Kontrollkästchen "Always on-Top" oder "automatisch ausblenden" auf der Eigenschaften Seite der Taskleiste aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="08464-104">Notifies an appbar that the taskbar's autohide or always-on-top state has changed that is, the user has selected or cleared the "Always on top" or "Auto hide" check box on the taskbar's property sheet.</span></span>


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a><span data-ttu-id="08464-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="08464-105">Parameters</span></span>

<span data-ttu-id="08464-106">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="08464-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08464-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08464-107">Return value</span></span>

<span data-ttu-id="08464-108">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="08464-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08464-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08464-109">Remarks</span></span>

<span data-ttu-id="08464-110">Eine appbar kann diese Benachrichtigungs Meldung verwenden, um den Status der Taskleiste, wenn gewünscht, auf die Konformität festzulegen.</span><span class="sxs-lookup"><span data-stu-id="08464-110">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="08464-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="08464-111">Requirements</span></span>



| <span data-ttu-id="08464-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08464-112">Requirement</span></span> | <span data-ttu-id="08464-113">Wert</span><span class="sxs-lookup"><span data-stu-id="08464-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08464-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08464-114">Minimum supported client</span></span><br/> | <span data-ttu-id="08464-115">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08464-115">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="08464-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08464-116">Minimum supported server</span></span><br/> | <span data-ttu-id="08464-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08464-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08464-118">Header</span><span class="sxs-lookup"><span data-stu-id="08464-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="08464-119"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="08464-119"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




