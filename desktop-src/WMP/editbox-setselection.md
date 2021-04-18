---
title: EditBox. setSelection
description: Die setSelection-Methode wählt den Text im Bearbeitungsfeld-Steuerelement vom angegebenen Start Index bis zum angegebenen endIndex aus.
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- EditBox. setSelection-Fenster Media Player
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364853"
---
# <a name="editboxsetselection"></a><span data-ttu-id="71f2b-104">EditBox. setSelection</span><span class="sxs-lookup"><span data-stu-id="71f2b-104">EDITBOX.setSelection</span></span>

<span data-ttu-id="71f2b-105">Die **setSelection** -Methode wählt den Text im Bearbeitungsfeld-Steuerelement vom angegebenen Start Index bis zum angegebenen endIndex aus.</span><span class="sxs-lookup"><span data-stu-id="71f2b-105">The **setSelection** method selects the text in the edit box control from the specified start index to the specified end index.</span></span>

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a><span data-ttu-id="71f2b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="71f2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f2b-107"><span id="start"></span><span id="START"></span>*begonnen*</span><span class="sxs-lookup"><span data-stu-id="71f2b-107"><span id="start"></span><span id="START"></span>*start*</span></span>
</dt> <dd>

<span data-ttu-id="71f2b-108">**Number** (**Long**), die den Zeichen Index der Anfangsposition des ausgewählten Texts enthält.</span><span class="sxs-lookup"><span data-stu-id="71f2b-108">**Number** (**long**) containing the character index of the starting position of the selected text.</span></span>

</dd> <dt>

<span data-ttu-id="71f2b-109"><span id="end"></span><span id="END"></span>*Schließlich*</span><span class="sxs-lookup"><span data-stu-id="71f2b-109"><span id="end"></span><span id="END"></span>*end*</span></span>
</dt> <dd>

<span data-ttu-id="71f2b-110">**Number** (**Long**), die den Zeichen Index der Endposition des ausgewählten Texts enthält.</span><span class="sxs-lookup"><span data-stu-id="71f2b-110">**Number** (**long**) containing the character index of the ending position of the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71f2b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71f2b-111">Return Value</span></span>

<span data-ttu-id="71f2b-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="71f2b-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71f2b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71f2b-113">Remarks</span></span>

<span data-ttu-id="71f2b-114">Wenn der Start Wert 0 und das Ende 1 ist, wird der gesamte Text im Bearbeitungsfeld-Steuerelement ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="71f2b-114">If the start is 0 and the end is  1, all of the text in the edit box control is selected.</span></span> <span data-ttu-id="71f2b-115">Wenn der Start Wert 1 ist, wird jede aktuelle Auswahl deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="71f2b-115">If the start is  1, any current selection is deselected.</span></span>

<span data-ttu-id="71f2b-116">Diese Methode kann nur aufgerufen werden, nachdem das Steuerelement sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="71f2b-116">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="71f2b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71f2b-117">Requirements</span></span>



| <span data-ttu-id="71f2b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71f2b-118">Requirement</span></span> | <span data-ttu-id="71f2b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="71f2b-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="71f2b-120">Version</span><span class="sxs-lookup"><span data-stu-id="71f2b-120">Version</span></span><br/> | <span data-ttu-id="71f2b-121">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="71f2b-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71f2b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71f2b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f2b-123">**EditBox-Element**</span><span class="sxs-lookup"><span data-stu-id="71f2b-123">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="71f2b-124">**EditBox. getSelectionEnd**</span><span class="sxs-lookup"><span data-stu-id="71f2b-124">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="71f2b-125">**EditBox. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="71f2b-125">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="71f2b-126">**EditBox. ReplaceSelection**</span><span class="sxs-lookup"><span data-stu-id="71f2b-126">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> </dl>

 

 





