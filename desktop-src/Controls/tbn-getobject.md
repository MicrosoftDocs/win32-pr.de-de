---
title: TBN_GETOBJECT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem ToolBar-Steuerelement gesendet, das den tbstyle \_ registerdrop-Stil verwendet, um ein Ablage Zielobjekt anzufordern, wenn der Zeiger über eine seiner Schaltflächen weitergeleitet wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- Windows-Steuerelemente für TBN_GETOBJECT Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ed144245e351ca4e872128e68fe658bde7c0066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102859"
---
# <a name="tbn_getobject-notification-code"></a><span data-ttu-id="df2d3-105">TBN- \_ GetObject-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="df2d3-105">TBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="df2d3-106">Wird von einem ToolBar-Steuerelement gesendet, das den [**tbstyle \_ registerdrop**](toolbar-control-and-button-styles.md) -Stil verwendet, um ein Ablage Zielobjekt anzufordern, wenn der Zeiger über eine seiner Schaltflächen weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="df2d3-106">Sent by a toolbar control that uses the [**TBSTYLE\_REGISTERDROP**](toolbar-control-and-button-styles.md) style to request a drop target object when the pointer passes over one of its buttons.</span></span> <span data-ttu-id="df2d3-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="df2d3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="df2d3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="df2d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df2d3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df2d3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df2d3-110">Ein Zeiger auf eine [**nmujectnotify**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) -Struktur, die Informationen über die Schaltfläche enthält, über die der Zeiger übergeben wurde und die Daten empfängt, die die Anwendung als Reaktion auf diesen Benachrichtigungs Code bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="df2d3-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the button that the pointer passed over and receives data the application provides in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df2d3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df2d3-111">Return value</span></span>

<span data-ttu-id="df2d3-112">Die Anwendung, die diesen Benachrichtigungs Code verarbeitet, muss NULL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="df2d3-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="df2d3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df2d3-113">Remarks</span></span>

<span data-ttu-id="df2d3-114">Um ein Objekt bereitzustellen, muss eine Anwendung Werte in einigen Membern der [**nmujectnotify**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) -Struktur bei *LPARAM* festlegen.</span><span class="sxs-lookup"><span data-stu-id="df2d3-114">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="df2d3-115">Das **pObject** -Element muss auf einen gültigen Objekt Zeiger festgelegt werden, und das **HRESULT** -Element muss auf ein Success-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="df2d3-115">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="df2d3-116">Um die Component Object Model (com)-Standards einzuhalten, erhöhen Sie immer den Verweis Zähler des Objekts, wenn Sie einen Objekt Zeiger bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="df2d3-116">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="df2d3-117">Wenn eine Anwendung kein Objekt bereitstellt, muss **pObject** auf **null** und **HRESULT** auf ein Fehlerflag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="df2d3-117">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="df2d3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df2d3-118">Requirements</span></span>



| <span data-ttu-id="df2d3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df2d3-119">Requirement</span></span> | <span data-ttu-id="df2d3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="df2d3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df2d3-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df2d3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="df2d3-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df2d3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df2d3-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df2d3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="df2d3-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df2d3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df2d3-125">Header</span><span class="sxs-lookup"><span data-stu-id="df2d3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="df2d3-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="df2d3-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





