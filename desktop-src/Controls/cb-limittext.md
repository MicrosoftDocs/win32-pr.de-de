---
title: CB_LIMITTEXT Meldung (Winuser. h)
description: Schränkt die Länge des Texts ein, den der Benutzer in das Bearbeitungs Steuerelement eines Kombinations Felds eingeben darf.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- Windows-Steuerelemente für CB_LIMITTEXT Meldung
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ea9ccd63bb1503e73aebdd584a53bc32bcb8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040595"
---
# <a name="cb_limittext-message"></a><span data-ttu-id="00be1-104">CB- \_ limittext Nachricht</span><span class="sxs-lookup"><span data-stu-id="00be1-104">CB\_LIMITTEXT message</span></span>

<span data-ttu-id="00be1-105">Schränkt die Länge des Texts ein, den der Benutzer in das Bearbeitungs Steuerelement eines Kombinations Felds eingeben darf.</span><span class="sxs-lookup"><span data-stu-id="00be1-105">Limits the length of the text the user may type into the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="00be1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00be1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00be1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00be1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00be1-108">Die maximale Anzahl von **tchars** , die vom Benutzer eingegeben werden können, ohne das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="00be1-108">The maximum number of **TCHARs** the user can enter, not including the terminating null character.</span></span> <span data-ttu-id="00be1-109">Wenn dieser Parameter 0 (null) ist, ist die Textlänge auf 0x7ffffffe-Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="00be1-109">If this parameter is zero, the text length is limited to 0x7FFFFFFE characters.</span></span>

</dd> <dt>

<span data-ttu-id="00be1-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00be1-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00be1-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="00be1-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00be1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00be1-112">Return value</span></span>

<span data-ttu-id="00be1-113">Der Rückgabewert ist immer " **true**".</span><span class="sxs-lookup"><span data-stu-id="00be1-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="00be1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00be1-114">Remarks</span></span>

<span data-ttu-id="00be1-115">Wenn das Kombinations Feld den [**\_ autohscroll**](combo-box-styles.md) -Stil "CBS" nicht aufweist, hat das Festlegen des Text Limits auf einen höheren Wert als die Größe des Bearbeitungs Steuer Elements keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="00be1-115">If the combo box does not have the [**CBS\_AUTOHSCROLL**](combo-box-styles.md) style, setting the text limit to be larger than the size of the edit control has no effect.</span></span>

<span data-ttu-id="00be1-116">Die **CB- \_ limittext** -Nachricht schränkt nur den Text ein, den der Benutzer eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="00be1-116">The **CB\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="00be1-117">Sie hat keine Auswirkung auf einen Text, der sich bereits im Bearbeitungs Steuerelement befindet, wenn die Nachricht gesendet wird, und wirkt sich auch nicht auf die Länge des Texts aus, der in das Bearbeitungs Steuerelement kopiert wird, wenn eine Zeichenfolge im Listenfeld ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="00be1-117">It has no effect on any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control when a string in the list box is selected.</span></span>

<span data-ttu-id="00be1-118">Der Standard Grenzwert für den Text, den ein Benutzer im Bearbeitungs Steuerelement eingeben kann, ist 30.000 **tchars**.</span><span class="sxs-lookup"><span data-stu-id="00be1-118">The default limit to the text a user can enter in the edit control is 30,000 **TCHARs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="00be1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00be1-119">Requirements</span></span>



| <span data-ttu-id="00be1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00be1-120">Requirement</span></span> | <span data-ttu-id="00be1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="00be1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00be1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00be1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="00be1-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00be1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="00be1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00be1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="00be1-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00be1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="00be1-126">Header</span><span class="sxs-lookup"><span data-stu-id="00be1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="00be1-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="00be1-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





