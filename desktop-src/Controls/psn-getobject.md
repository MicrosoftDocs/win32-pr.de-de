---
title: PSN_GETOBJECT Benachrichtigungs Code (prsht. h)
description: Wird von einem Eigenschaften Blatt gesendet, um ein Ablage Zielobjekt anzufordern, wenn der Cursor über eine der Schaltflächen des Registerkarten-Steuer Elements weitergeleitet wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- Windows-Steuerelemente für PSN_GETOBJECT Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_GETOBJECT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0a039cf97dee1d1f1168894bb167c06de10d38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040312"
---
# <a name="psn_getobject-notification-code"></a><span data-ttu-id="a3c45-105">PSN- \_ GetObject-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a3c45-105">PSN\_GETOBJECT notification code</span></span>

<span data-ttu-id="a3c45-106">Wird von einem Eigenschaften Blatt gesendet, um ein Ablage Zielobjekt anzufordern, wenn der Cursor über eine der Schaltflächen des Registerkarten-Steuer Elements weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="a3c45-106">Sent by a property sheet to request a drop target object when the cursor passes over one of the tab control's buttons.</span></span> <span data-ttu-id="a3c45-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a3c45-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a3c45-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3c45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3c45-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3c45-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3c45-110">Zeiger auf eine [**nmujectnotify**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) -Struktur, die bei einem Eintrag Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="a3c45-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that, on entry, contains information about the notification code.</span></span> <span data-ttu-id="a3c45-111">Wenn dieser Benachrichtigungs Code verarbeitet wird, müssen Sie Objektinformationen in diese Struktur einfügen.</span><span class="sxs-lookup"><span data-stu-id="a3c45-111">If this notification code is processed, you must insert object information into this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3c45-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3c45-112">Return value</span></span>

<span data-ttu-id="a3c45-113">Die Anwendung, die diesen Benachrichtigungs Code verarbeitet, muss NULL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a3c45-113">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3c45-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3c45-114">Remarks</span></span>

<span data-ttu-id="a3c45-115">Um ein Objekt bereitzustellen, muss eine Anwendung Werte in einigen Membern der [**nmujectnotify**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) -Struktur bei *LPARAM* festlegen.</span><span class="sxs-lookup"><span data-stu-id="a3c45-115">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="a3c45-116">Das **pObject** -Element muss auf einen gültigen Objekt Zeiger festgelegt werden, und das **HRESULT** -Element muss auf ein Success-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a3c45-116">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="a3c45-117">Um die Component Object Model (com)-Standards einzuhalten, erhöhen Sie immer den Verweis Zähler des Objekts, wenn Sie einen Objekt Zeiger bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a3c45-117">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="a3c45-118">Wenn eine Anwendung kein Objekt bereitstellt, muss **pObject** auf **null** und **HRESULT** auf ein Fehlerflag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a3c45-118">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

> [!Note]  
> <span data-ttu-id="a3c45-119">Dieser Benachrichtigungs Code wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3c45-119">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a3c45-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3c45-120">Requirements</span></span>



| <span data-ttu-id="a3c45-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3c45-121">Requirement</span></span> | <span data-ttu-id="a3c45-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a3c45-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c45-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3c45-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a3c45-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3c45-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a3c45-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3c45-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a3c45-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3c45-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a3c45-127">Header</span><span class="sxs-lookup"><span data-stu-id="a3c45-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3c45-128"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3c45-128"><dt>Prsht.h</dt></span></span> </dl> |



 

 





