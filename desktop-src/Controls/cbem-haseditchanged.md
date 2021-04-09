---
title: CBEM_HASEDITCHANGED Meldung (kommstrg. h)
description: Bestimmt, ob der Benutzer den Text eines ComboBoxEx-Bearbeitungs Steuer Elements geändert hat.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- Windows-Steuerelemente für CBEM_HASEDITCHANGED Meldung
topic_type:
- apiref
api_name:
- CBEM_HASEDITCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5234b816a2ec080449ade072981b489968df8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957192"
---
# <a name="cbem_haseditchanged-message"></a><span data-ttu-id="e7169-104">CBEM \_ haseditchanged-Meldung</span><span class="sxs-lookup"><span data-stu-id="e7169-104">CBEM\_HASEDITCHANGED message</span></span>

<span data-ttu-id="e7169-105">Bestimmt, ob der Benutzer den Text eines ComboBoxEx-Bearbeitungs Steuer Elements geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e7169-105">Determines whether the user has changed the text of a ComboBoxEx edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7169-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7169-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7169-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7169-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e7169-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e7169-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e7169-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7169-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e7169-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e7169-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7169-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7169-111">Return value</span></span>

<span data-ttu-id="e7169-112">Gibt **true** zurück, wenn der Text im Bearbeitungsfeld des Steuer Elements geändert wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="e7169-112">Returns **TRUE** if the text in the control's edit box has been changed, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7169-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7169-113">Remarks</span></span>

<span data-ttu-id="e7169-114">Ein ComboBoxEx-Steuerelement verwendet ein Bearbeitungsfeld-Steuerelement, wenn es auf den [**CBS- \_ Dropdown**](combo-box-styles.md) Stil festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e7169-114">A ComboBoxEx control uses an edit box control when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="e7169-115">Sie können das Fenster Handle des Bearbeitungsfeld Steuer Elements abrufen, indem Sie eine [**CBEM \_ geteditcontrol**](cbem-geteditcontrol.md) -Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="e7169-115">You can retrieve the edit box control's window handle by sending a [**CBEM\_GETEDITCONTROL**](cbem-geteditcontrol.md) message.</span></span>

<span data-ttu-id="e7169-116">Wenn der Benutzer mit der Bearbeitung beginnt, erhalten Sie eine [cben \_ BeginEdit](cben-beginedit.md) -Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="e7169-116">When the user begins editing, you will receive a [CBEN\_BEGINEDIT](cben-beginedit.md) notification.</span></span> <span data-ttu-id="e7169-117">Wenn die Bearbeitung oder der Fokus geändert wird, erhalten Sie eine [cben \_ EndEdit](cben-endedit.md) -Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="e7169-117">When editing is complete, or the focus changes, you will receive a [CBEN\_ENDEDIT](cben-endedit.md) notification.</span></span> <span data-ttu-id="e7169-118">Die Meldung " **CBEM \_ haseditchanged** " ist nur hilfreich, um zu bestimmen, ob der Text geändert wurde, wenn er vor der cben- \_ EndEdit-Benachrichtigung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7169-118">The **CBEM\_HASEDITCHANGED** message is only useful for determining whether the text has been changed if it is sent before the CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="e7169-119">Wenn die Nachricht später gesendet wird, wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e7169-119">If the message is sent afterward, it will return **FALSE**.</span></span> <span data-ttu-id="e7169-120">Angenommen, der Benutzer beginnt, den Text im Bearbeitungsfeld zu bearbeiten, ändert jedoch den Fokus und erzeugt eine cben \_ EndEdit-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="e7169-120">For example, suppose the user starts to edit the text in the edit box but changes focus, generating a CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="e7169-121">Wenn Sie dann eine **CBEM \_ haseditchanged** -Nachricht senden, wird **false** zurückgegeben, auch wenn der Text geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e7169-121">If you then send a **CBEM\_HASEDITCHANGED** message, it will return **FALSE**, even though the text has been changed.</span></span>

<span data-ttu-id="e7169-122">Der [**\_ einfache CBS**](combo-box-styles.md) -Stil funktioniert mit **CBEM \_ haseditchanged** nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="e7169-122">The [**CBS\_SIMPLE**](combo-box-styles.md) style does not work correctly with **CBEM\_HASEDITCHANGED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7169-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7169-123">Requirements</span></span>



| <span data-ttu-id="e7169-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7169-124">Requirement</span></span> | <span data-ttu-id="e7169-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e7169-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7169-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7169-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e7169-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7169-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7169-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7169-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e7169-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7169-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7169-130">Header</span><span class="sxs-lookup"><span data-stu-id="e7169-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7169-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7169-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





