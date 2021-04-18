---
title: Idwrite-fontsetbuilder addfontfacereferenzierungsmethoden (dwrite \_ 3. h)
description: Fügt einen Verweis auf eine Schriftart zum erstellten Satz hinzu.
ms.assetid: 2543720f-1b5a-ca1d-9e24-3fcd61a4de37
keywords:
- Addfontfacereferenzierungsmethoden direkt schreiben
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3c20ca2832bfce3696a98c22730580442f621469
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372155"
---
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a><span data-ttu-id="06610-104">Idwrite-fontsetbuilder:: addfontfacereferenzierungsmethoden</span><span class="sxs-lookup"><span data-stu-id="06610-104">IDWriteFontSetBuilder::AddFontFaceReference methods</span></span>

<span data-ttu-id="06610-105">Fügt einen Verweis auf eine Schriftart zum erstellten Satz hinzu.</span><span class="sxs-lookup"><span data-stu-id="06610-105">Adds a reference to a font to the set being built.</span></span>

### <a name="overload-list"></a><span data-ttu-id="06610-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="06610-106">Overload list</span></span>



| <span data-ttu-id="06610-107">Methode</span><span class="sxs-lookup"><span data-stu-id="06610-107">Method</span></span>                                                                                                                                           | <span data-ttu-id="06610-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06610-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06610-109">[**Addfontfakereferenzierung (idschreitefontfakereferenzierung \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span><span class="sxs-lookup"><span data-stu-id="06610-109">[**AddFontFaceReference(IDWriteFontFaceReference\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span></span>                                         | <span data-ttu-id="06610-110">Fügt einen Verweis auf eine Schriftart zum erstellten Satz hinzu.</span><span class="sxs-lookup"><span data-stu-id="06610-110">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="06610-111">Die erforderlichen Metadaten werden automatisch aus der Schriftart extrahiert, wenn createfontset aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="06610-111">The necessary metadata will automatically be extracted from the font upon calling CreateFontSet.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="06610-112">[**Addfontfakereferenzierung (idschreitefontfakereferenzierung \* , Konstante dwrite- \_ Schriftart \_ Eigenschaft \* , UInt32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span><span class="sxs-lookup"><span data-stu-id="06610-112">[**AddFontFaceReference(IDWriteFontFaceReference\*, const DWRITE\_FONT\_PROPERTY\*, UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span></span> | <span data-ttu-id="06610-113">Fügt einen Verweis auf eine Schriftart zum erstellten Satz hinzu.</span><span class="sxs-lookup"><span data-stu-id="06610-113">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="06610-114">Der Aufrufer liefert genug Informationen, um zu suchen, und es wird vermieden, dass die möglicherweise nicht lokale Schriftart geöffnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="06610-114">The caller supplies enough information to search on, avoiding the need to open the potentially non-local font.</span></span> <span data-ttu-id="06610-115">Alle Eigenschaften, die nicht vom Aufrufer bereitgestellt werden, fehlen, und diese Eigenschaften sind nicht als Filter in getmatchingfonts verfügbar.</span><span class="sxs-lookup"><span data-stu-id="06610-115">Any properties not supplied by the caller will be missing, and those properties will not be available as filters in GetMatchingFonts.</span></span> <span data-ttu-id="06610-116">GetPropertyValues für fehlende Eigenschaften gibt eine leere Zeichen folgen Liste zurück.</span><span class="sxs-lookup"><span data-stu-id="06610-116">GetPropertyValues for missing properties will return an empty string list.</span></span> <span data-ttu-id="06610-117">Die übergebenen Eigenschaften sollten im Allgemeinen mit dem tatsächlichen Schriftart Inhalt konsistent sein, Sie müssen jedoch nicht sein.</span><span class="sxs-lookup"><span data-stu-id="06610-117">The properties passed should generally be consistent with the actual font contents, but they need not be.</span></span> <span data-ttu-id="06610-118">Sie könnten z. b. eine Schriftart mit einem anderen Namen oder eindeutigen Bezeichner als Alias verwenden, oder Sie können benutzerdefinierte Tags festlegen, die nicht in der eigentlichen Schriftart vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="06610-118">You could, for example, alias a font using a different name or unique identifier, or you could set custom tags not present in the actual font.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="06610-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06610-119">Requirements</span></span>



| <span data-ttu-id="06610-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06610-120">Requirement</span></span> | <span data-ttu-id="06610-121">Wert</span><span class="sxs-lookup"><span data-stu-id="06610-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06610-122">Header</span><span class="sxs-lookup"><span data-stu-id="06610-122">Header</span></span><br/> | <dl> <span data-ttu-id="06610-123"><dt>Dwrite \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="06610-123"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06610-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06610-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06610-125">**Idschreitefontsetbuilder**</span><span class="sxs-lookup"><span data-stu-id="06610-125">**IDWriteFontSetBuilder**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

<span data-ttu-id="06610-126">�</span><span class="sxs-lookup"><span data-stu-id="06610-126">�</span></span>

<span data-ttu-id="06610-127">�</span><span class="sxs-lookup"><span data-stu-id="06610-127">�</span></span>
