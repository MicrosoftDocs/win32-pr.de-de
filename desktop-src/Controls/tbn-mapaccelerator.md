---
title: TBN_MAPACCELERATOR Benachrichtigungs Code (kommctrl. h)
description: Fordert den Index der Schaltfläche auf der Symbolleiste an, die dem angegebenen Beschleunigungs Zeichen entspricht. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- Windows-Steuerelemente für TBN_MAPACCELERATOR Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b20f1908f441c38e23aa7428f8c8edb8a192c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949409"
---
# <a name="tbn_mapaccelerator-notification-code"></a><span data-ttu-id="8c21c-105">TBN- \_ mapaccelerator-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="8c21c-105">TBN\_MAPACCELERATOR notification code</span></span>

<span data-ttu-id="8c21c-106">Fordert den Index der Schaltfläche auf der Symbolleiste an, die dem angegebenen Beschleunigungs Zeichen entspricht.</span><span class="sxs-lookup"><span data-stu-id="8c21c-106">Requests the index of the button in the toolbar corresponding to the specified accelerator character.</span></span> <span data-ttu-id="8c21c-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="8c21c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8c21c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c21c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c21c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c21c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c21c-110">Ein Zeiger auf eine [**nmchar**](/windows/win32/api/commctrl/ns-commctrl-nmchar) -Struktur, die das Tastenkombination-Zeichen enthält und den Index der entsprechenden Schaltfläche empfängt.</span><span class="sxs-lookup"><span data-stu-id="8c21c-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains the accelerator key character and that receives the index of the corresponding button.</span></span> <span data-ttu-id="8c21c-111">Das Feld " **dwitemnext** " ist "-1", wenn die Zugriffstaste keinem Befehl entspricht.</span><span class="sxs-lookup"><span data-stu-id="8c21c-111">The **dwItemNext** field is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c21c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c21c-112">Return value</span></span>

<span data-ttu-id="8c21c-113">TRUE, wenn **nmchar. dwitemnext** auf einen Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8c21c-113">TRUE if **NMCHAR.dwItemNext** is set to a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c21c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c21c-114">Requirements</span></span>



| <span data-ttu-id="8c21c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c21c-115">Requirement</span></span> | <span data-ttu-id="8c21c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8c21c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c21c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c21c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c21c-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c21c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c21c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c21c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c21c-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c21c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c21c-121">Header</span><span class="sxs-lookup"><span data-stu-id="8c21c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c21c-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c21c-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





