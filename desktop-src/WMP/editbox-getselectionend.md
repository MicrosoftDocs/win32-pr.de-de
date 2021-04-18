---
title: EditBox. getSelectionEnd
description: Die getSelectionEnd-Methode ruft die Endposition des ausgewählten Texts im EditBox-Steuerelement ab.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- EditBox. getSelectionEnd-Windows-Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f27c2974360e7e77becfa67a27b4e96b529ad1e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372772"
---
# <a name="editboxgetselectionend"></a><span data-ttu-id="24151-104">EditBox. getSelectionEnd</span><span class="sxs-lookup"><span data-stu-id="24151-104">EDITBOX.getSelectionEnd</span></span>

<span data-ttu-id="24151-105">Die **getSelectionEnd** -Methode ruft die Endposition des ausgewählten Texts im EditBox-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="24151-105">The **getSelectionEnd** method retrieves the ending position of the selected text in the editbox control.</span></span>

``` syntax
        elementID.getSelectionEnd()
```

## <a name="parameters"></a><span data-ttu-id="24151-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="24151-106">Parameters</span></span>

<span data-ttu-id="24151-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="24151-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24151-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24151-108">Return Value</span></span>

<span data-ttu-id="24151-109">Diese Methode gibt eine **Zahl** (**Long**) zurück.</span><span class="sxs-lookup"><span data-stu-id="24151-109">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="24151-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24151-110">Remarks</span></span>

<span data-ttu-id="24151-111">Wenn kein Text ausgewählt ist, gibt diese Methode die Position der Einfügemarke zurück.</span><span class="sxs-lookup"><span data-stu-id="24151-111">If no text is selected, this method returns the position of the insertion point.</span></span>

<span data-ttu-id="24151-112">Wenn das Steuerelement mehrzeilige Elemente ist, gibt diese Methode den Zeichen Index im-Steuerelement zurück, nicht den Zeilen Index.</span><span class="sxs-lookup"><span data-stu-id="24151-112">If the control is multiline, this method returns the character index in the control, not the line index.</span></span>

<span data-ttu-id="24151-113">Diese Methode kann nur aufgerufen werden, nachdem das Steuerelement sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="24151-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="24151-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24151-114">Requirements</span></span>



| <span data-ttu-id="24151-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24151-115">Requirement</span></span> | <span data-ttu-id="24151-116">Wert</span><span class="sxs-lookup"><span data-stu-id="24151-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="24151-117">Version</span><span class="sxs-lookup"><span data-stu-id="24151-117">Version</span></span><br/> | <span data-ttu-id="24151-118">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="24151-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24151-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24151-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24151-120">**EditBox-Element**</span><span class="sxs-lookup"><span data-stu-id="24151-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="24151-121">**EditBox. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="24151-121">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="24151-122">**EditBox. ReplaceSelection**</span><span class="sxs-lookup"><span data-stu-id="24151-122">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> <dt>

[<span data-ttu-id="24151-123">**EditBox. setSelection**</span><span class="sxs-lookup"><span data-stu-id="24151-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





