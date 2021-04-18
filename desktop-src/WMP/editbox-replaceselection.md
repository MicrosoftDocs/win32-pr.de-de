---
title: EditBox. ReplaceSelection
description: Die ReplaceSelection-Methode ersetzt die aktuelle Auswahl durch den angegebenen Text.
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- EditBox. ReplaceSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368328"
---
# <a name="editboxreplaceselection"></a><span data-ttu-id="1f400-104">EditBox. ReplaceSelection</span><span class="sxs-lookup"><span data-stu-id="1f400-104">EDITBOX.replaceSelection</span></span>

<span data-ttu-id="1f400-105">Die **ReplaceSelection** -Methode ersetzt die aktuelle Auswahl durch den angegebenen Text.</span><span class="sxs-lookup"><span data-stu-id="1f400-105">The **replaceSelection** method replaces the current selection with the specified text.</span></span>

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a><span data-ttu-id="1f400-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f400-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f400-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*NewValue*</span><span class="sxs-lookup"><span data-stu-id="1f400-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*</span></span>
</dt> <dd>

<span data-ttu-id="1f400-108">**Zeichenfolge** , die den Text enthält, um den markierten Text zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="1f400-108">**String** containing the text to replace the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f400-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f400-109">Return Value</span></span>

<span data-ttu-id="1f400-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1f400-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f400-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f400-111">Remarks</span></span>

<span data-ttu-id="1f400-112">Wenn kein Text ausgewählt ist, wird der Ersetzungstext an der aktuellen Position der Einfügemarke eingefügt.</span><span class="sxs-lookup"><span data-stu-id="1f400-112">If there is no text selected, the replacement text is inserted at the current location of the insertion point.</span></span>

<span data-ttu-id="1f400-113">Diese Methode kann nur aufgerufen werden, nachdem das Steuerelement sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="1f400-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f400-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f400-114">Requirements</span></span>



| <span data-ttu-id="1f400-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f400-115">Requirement</span></span> | <span data-ttu-id="1f400-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1f400-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="1f400-117">Version</span><span class="sxs-lookup"><span data-stu-id="1f400-117">Version</span></span><br/> | <span data-ttu-id="1f400-118">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="1f400-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f400-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f400-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f400-120">**EditBox-Element**</span><span class="sxs-lookup"><span data-stu-id="1f400-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="1f400-121">**EditBox. getSelectionEnd**</span><span class="sxs-lookup"><span data-stu-id="1f400-121">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="1f400-122">**EditBox. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="1f400-122">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="1f400-123">**EditBox. setSelection**</span><span class="sxs-lookup"><span data-stu-id="1f400-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





