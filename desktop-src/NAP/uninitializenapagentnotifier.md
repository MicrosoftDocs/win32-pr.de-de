---
title: Uninitializenapagentnotifier-Funktion (naputil. h)
description: Abonniert den aufrufenden Prozess von NAPAgent-Status Änderungs Benachrichtigungen und Benachrichtigungen über Quarantäne Zustandsänderungen.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- Uninitializenapagentnotifier-Funktion NAP
topic_type:
- apiref
api_name:
- UninitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d68b43fba64be82908d73803113f871b08c93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391774"
---
# <a name="uninitializenapagentnotifier-function"></a><span data-ttu-id="f55cc-104">Uninitializenapagentnotifier-Funktion</span><span class="sxs-lookup"><span data-stu-id="f55cc-104">UninitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="f55cc-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f55cc-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f55cc-106">Die **uninitializenapagentnotifier** -Funktion hebt den aufrufenden Prozess von NAPAgent-Status Änderungs Benachrichtigungen und Benachrichtigungen über Quarantäne Zustandsänderungen auf.</span><span class="sxs-lookup"><span data-stu-id="f55cc-106">The **UninitializeNapAgentNotifier** function unsubscribes the calling process from NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="f55cc-107">Diese Benachrichtigungen werden vom NAPAgent-Dienst bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f55cc-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="f55cc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f55cc-108">Syntax</span></span>


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a><span data-ttu-id="f55cc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f55cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f55cc-110">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f55cc-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f55cc-111">Ein [**napnotifytype**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) -Wert, der den Typ der Dienst Benachrichtigungen angibt, von denen abgemeldet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f55cc-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to unsubscribe from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f55cc-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f55cc-112">Return value</span></span>

<span data-ttu-id="f55cc-113">Diese Funktion verfügt über keine Rückgabewerte.</span><span class="sxs-lookup"><span data-stu-id="f55cc-113">This function has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f55cc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f55cc-114">Remarks</span></span>

<span data-ttu-id="f55cc-115">Diese Funktion ist nicht threadsicher.</span><span class="sxs-lookup"><span data-stu-id="f55cc-115">This function is not thread safe.</span></span>

<span data-ttu-id="f55cc-116">Jeder Prozess, der die NAPAgent-Dienst Benachrichtigungen des angegebenen *Typs* abonniert hat, muss **uninitializenapagentnotifier** anrufen, um Benachrichtigungen zu kündigen.</span><span class="sxs-lookup"><span data-stu-id="f55cc-116">Each process subscribed to NapAgent service notifications of the specified *type* must call **UninitializeNapAgentNotifier** to unsubscribe from notifications.</span></span> <span data-ttu-id="f55cc-117">Wenn ein Prozess mehr als einen Benachrichtigungstyp abonniert, muss er für jeden Benachrichtigungstyp einmal **uninitializenapagentnotifier** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f55cc-117">If a process is subscribed to more than one type of notification, it must call **UninitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="f55cc-118">Diese Funktion führt nicht automatisch zu einem Fehler, wenn der Prozess zuvor nicht [**initializenapagentnotifier**](initializenapagentnotifier.md) für den Benachrichtigungstyp aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="f55cc-118">This function will fail silently if the process had not previously called [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) for the notification type.</span></span>

## <a name="requirements"></a><span data-ttu-id="f55cc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f55cc-119">Requirements</span></span>



| <span data-ttu-id="f55cc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f55cc-120">Requirement</span></span> | <span data-ttu-id="f55cc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f55cc-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f55cc-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f55cc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f55cc-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f55cc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f55cc-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f55cc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f55cc-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f55cc-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f55cc-126">Header</span><span class="sxs-lookup"><span data-stu-id="f55cc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f55cc-127"><dt>Naputil. h</dt></span><span class="sxs-lookup"><span data-stu-id="f55cc-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="f55cc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f55cc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f55cc-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f55cc-129"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f55cc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f55cc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f55cc-131">**Initializenapagentnotifier**</span><span class="sxs-lookup"><span data-stu-id="f55cc-131">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
</dt> </dl>

 

 





