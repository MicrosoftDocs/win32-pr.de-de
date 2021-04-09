---
title: PSM_ISDIALOGMESSAGE Meldung (prsht. h)
description: Übergibt eine Meldung an ein Eigenschaften Blatt und gibt an, ob das Dialogfeld die Nachricht verarbeitet hat. Sie können diese Nachricht explizit oder mithilfe des propsheet \_ IsDialogMessage-Makros senden.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- Windows-Steuerelemente für PSM_ISDIALOGMESSAGE Meldung
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b753fc849d76e3ac5071dd85bdd94950460fbb10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858938"
---
# <a name="psm_isdialogmessage-message"></a><span data-ttu-id="00929-105">PSM \_ IsDialogMessage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="00929-105">PSM\_ISDIALOGMESSAGE message</span></span>

<span data-ttu-id="00929-106">Übergibt eine Meldung an ein Eigenschaften Blatt und gibt an, ob das Dialogfeld die Nachricht verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="00929-106">Passes a message to a property sheet dialog box and indicates whether the dialog box processed the message.</span></span> <span data-ttu-id="00929-107">Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="00929-107">You can send this message explicitly or by using the [**PropSheet\_IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="00929-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="00929-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00929-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00929-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00929-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="00929-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="00929-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00929-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00929-112">Zeiger auf eine [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur, die die zu überprüfende Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="00929-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00929-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00929-113">Return value</span></span>

<span data-ttu-id="00929-114">Gibt " **true** " zurück, wenn die Nachricht verarbeitet wurde, oder " **false** ", wenn die Meldung nicht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="00929-114">Returns **TRUE** if the message has been processed, or **FALSE** if the message has not been processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="00929-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00929-115">Remarks</span></span>

<span data-ttu-id="00929-116">Die Nachrichten Schleife sollte die **PSM \_ IsDialogMessage** -Nachricht mit nicht modalem Eigenschaften Blättern verwenden, um Nachrichten an das Eigenschaften Blatt zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="00929-116">Your message loop should use the **PSM\_ISDIALOGMESSAGE** message with modeless property sheets to pass messages to the property sheet dialog box.</span></span> <span data-ttu-id="00929-117">Verwenden Sie auf Systemen, die Unicode unterstützen, die Unicode-Versionen der Funktionen [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) und [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**getmessagew** und **peekmessagew**) zum Abrufen von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="00929-117">On systems that support Unicode, use the Unicode versions of the [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) functions (**GetMessageW** and **PeekMessageW**) to retrieve messages.</span></span>

<span data-ttu-id="00929-118">Wenn der Rückgabewert angibt, dass die Nachricht verarbeitet wurde, darf Sie nicht an die Funktion [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) oder [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="00929-118">If the return value indicates that the message was processed, it must not be passed to the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) or [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function.</span></span>

> [!Note]  
> <span data-ttu-id="00929-119">Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="00929-119">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="00929-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00929-120">Requirements</span></span>



| <span data-ttu-id="00929-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00929-121">Requirement</span></span> | <span data-ttu-id="00929-122">Wert</span><span class="sxs-lookup"><span data-stu-id="00929-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00929-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00929-123">Minimum supported client</span></span><br/> | <span data-ttu-id="00929-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00929-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="00929-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00929-125">Minimum supported server</span></span><br/> | <span data-ttu-id="00929-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00929-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="00929-127">Header</span><span class="sxs-lookup"><span data-stu-id="00929-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="00929-128"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="00929-128"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00929-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00929-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00929-130">**Eigenschaften Blatt**</span><span class="sxs-lookup"><span data-stu-id="00929-130">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

