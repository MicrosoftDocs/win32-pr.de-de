---
title: EditBox. getSelectionStart
description: Die getSelectionStart-Methode ruft die Anfangsposition des ausgewählten Texts im EditBox-Steuerelement ab.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- EditBox. getSelectionStart Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2508119e5b1d46d09b3531582e86caad7e7facbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362178"
---
# <a name="editboxgetselectionstart"></a><span data-ttu-id="f5a5c-104">EditBox. getSelectionStart</span><span class="sxs-lookup"><span data-stu-id="f5a5c-104">EDITBOX.getSelectionStart</span></span>

<span data-ttu-id="f5a5c-105">Die **getSelectionStart** -Methode ruft die Anfangsposition des ausgewählten Texts im EditBox-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-105">The **getSelectionStart** method retrieves the starting position of the selected text in the editbox control.</span></span>

``` syntax
        elementID.getSelectionStart()
```

## <a name="parameters"></a><span data-ttu-id="f5a5c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5a5c-106">Parameters</span></span>

<span data-ttu-id="f5a5c-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5a5c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5a5c-108">Return Value</span></span>

<span data-ttu-id="f5a5c-109">Diese Methode gibt eine **Zahl** (**Long**) zurück.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-109">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a5c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5a5c-110">Remarks</span></span>

<span data-ttu-id="f5a5c-111">Wenn kein Text ausgewählt ist, gibt diese Methode die Position der Einfügemarke zurück.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-111">If no text is selected, this method returns the position of the insertion point.</span></span>

<span data-ttu-id="f5a5c-112">Wenn das Steuerelement mehrzeilige Elemente ist, gibt diese Methode den Zeichen Index im-Steuerelement zurück, nicht den Zeilen Index.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-112">If the control is multiline, this method returns the character index in the control, not the line index.</span></span>

<span data-ttu-id="f5a5c-113">Diese Methode kann nur aufgerufen werden, nachdem das Steuerelement sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="f5a5c-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a5c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5a5c-114">Requirements</span></span>



| <span data-ttu-id="f5a5c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5a5c-115">Requirement</span></span> | <span data-ttu-id="f5a5c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f5a5c-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="f5a5c-117">Version</span><span class="sxs-lookup"><span data-stu-id="f5a5c-117">Version</span></span><br/> | <span data-ttu-id="f5a5c-118">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="f5a5c-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5a5c-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5a5c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a5c-120">**EditBox-Element**</span><span class="sxs-lookup"><span data-stu-id="f5a5c-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="f5a5c-121">**EditBox. getSelectionEnd**</span><span class="sxs-lookup"><span data-stu-id="f5a5c-121">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="f5a5c-122">**EditBox. ReplaceSelection**</span><span class="sxs-lookup"><span data-stu-id="f5a5c-122">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> <dt>

[<span data-ttu-id="f5a5c-123">**EditBox. setSelection**</span><span class="sxs-lookup"><span data-stu-id="f5a5c-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





