---
title: RBN_GETOBJECT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, das mit dem Register Drop-Stil von RB erstellt \_ wird, wenn ein Objekt über ein Band im-Steuerelement gezogen wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- Windows-Steuerelemente für RBN_GETOBJECT Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a390bc5c5f74a577805ca8ae1128fbb24e6b10b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104775"
---
# <a name="rbn_getobject-notification-code"></a><span data-ttu-id="a21c0-105">RBN- \_ GetObject-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a21c0-105">RBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="a21c0-106">Wird von einem Grund leisten-Steuerelement gesendet, das mit dem [**\_ Register Drop**](rebar-control-styles.md) -Stil von RB erstellt wird, wenn ein Objekt über ein Band im-Steuerelement gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="a21c0-106">Sent by a rebar control created with the [**RBS\_REGISTERDROP**](rebar-control-styles.md) style when an object is dragged over a band in the control.</span></span> <span data-ttu-id="a21c0-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a21c0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a21c0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a21c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a21c0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a21c0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a21c0-110">Ein Zeiger auf eine [**nmujectnotify**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) -Struktur, die Informationen über das Band enthält, über das das Objekt gezogen wird. Außerdem werden die Daten, die von der empfangenden Anwendung als Reaktion auf diesen Benachrichtigungs Code bereitgestellt werden, empfangen.</span><span class="sxs-lookup"><span data-stu-id="a21c0-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the band that the object is dragged over and also receives the data provided by the receiving application in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a21c0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a21c0-111">Return value</span></span>

<span data-ttu-id="a21c0-112">Der Rückgabewert für diesen Benachrichtigungs Code muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a21c0-112">The return value for this notification code must be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a21c0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a21c0-113">Remarks</span></span>

<span data-ttu-id="a21c0-114">Um den RBN- \_ GetObject-Benachrichtigungs Code zu erhalten, initialisieren Sie OLE mit einem Aufrufen von [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) oder [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span><span class="sxs-lookup"><span data-stu-id="a21c0-114">To receive the RBN\_GETOBJECT notification code, initialize OLE with a call to [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) or [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span></span>

## <a name="requirements"></a><span data-ttu-id="a21c0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a21c0-115">Requirements</span></span>



| <span data-ttu-id="a21c0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a21c0-116">Requirement</span></span> | <span data-ttu-id="a21c0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a21c0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a21c0-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a21c0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a21c0-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a21c0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a21c0-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a21c0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a21c0-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a21c0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a21c0-122">Header</span><span class="sxs-lookup"><span data-stu-id="a21c0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a21c0-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a21c0-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

