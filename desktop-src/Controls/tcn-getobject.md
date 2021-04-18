---
title: TCN_GETOBJECT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Registerkarten-Steuerelement gesendet, wenn es den erweiterten TCS \_ \_ -registerdrop-Stil hat und ein Objekt über ein Registerkarten Element im-Steuerelement gezogen wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- Windows-Steuerelemente für TCN_GETOBJECT Benachrichtigungs
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340304"
---
# <a name="tcn_getobject-notification-code"></a><span data-ttu-id="341fc-105">TCN \_ GetObject-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="341fc-105">TCN\_GETOBJECT notification code</span></span>

<span data-ttu-id="341fc-106">Wird von einem Registerkarten-Steuerelement gesendet, wenn es den erweiterten [**TCS- \_ \_ registerdrop**](tab-control-extended-styles.md) -Stil hat und ein Objekt über ein Registerkarten Element im-Steuerelement gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="341fc-106">Sent by a tab control when it has the [**TCS\_EX\_REGISTERDROP**](tab-control-extended-styles.md) extended style and an object is dragged over a tab item in the control.</span></span> <span data-ttu-id="341fc-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="341fc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="341fc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="341fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="341fc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="341fc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="341fc-110">Zeiger auf eine [**nmujectnotify**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) -Struktur, die Informationen über das Registerkarten Element enthält, über das das Objekt gezogen wird, und empfängt Daten empfängt, die von der Anwendung als Reaktion auf diese Nachricht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="341fc-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the tab item the object is dragged over and receives data the application returns in response to this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="341fc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="341fc-111">Return value</span></span>

<span data-ttu-id="341fc-112">Die Anwendung, die diesen Benachrichtigungs Code verarbeitet, muss NULL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="341fc-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="341fc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="341fc-113">Requirements</span></span>



| <span data-ttu-id="341fc-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="341fc-114">Requirement</span></span> | <span data-ttu-id="341fc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="341fc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="341fc-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="341fc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="341fc-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="341fc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="341fc-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="341fc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="341fc-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="341fc-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="341fc-120">Header</span><span class="sxs-lookup"><span data-stu-id="341fc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="341fc-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="341fc-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





