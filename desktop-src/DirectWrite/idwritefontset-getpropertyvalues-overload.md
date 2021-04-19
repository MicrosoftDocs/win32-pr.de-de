---
title: Idwrite-FONTSET GetPropertyValues-Methoden (dwrite \_ 3. h)
description: Gibt Eigenschaftswerte für den Schriftart Satz zurück.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- GetPropertyValues-Methoden direktes Schreiben
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3d135a63be987a4999d898c8e9c7d84251c8ece3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354176"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a><span data-ttu-id="6de87-104">Idwrite Test FONTSET:: GetPropertyValues-Methoden</span><span class="sxs-lookup"><span data-stu-id="6de87-104">IDWriteFontSet::GetPropertyValues methods</span></span>

<span data-ttu-id="6de87-105">Gibt Eigenschaftswerte für den Schriftart Satz zurück.</span><span class="sxs-lookup"><span data-stu-id="6de87-105">Returns property values for the font set.</span></span>

### <a name="overload-list"></a><span data-ttu-id="6de87-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="6de87-106">Overload list</span></span>



| <span data-ttu-id="6de87-107">Methode</span><span class="sxs-lookup"><span data-stu-id="6de87-107">Method</span></span>                                                                                                                                   | <span data-ttu-id="6de87-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6de87-108">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de87-109">[**GetPropertyValues (Eigenschaften-ID der dwrite- \_ Schriftart \_ \_ , idschreitestringlist \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="6de87-109">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span>                       | <span data-ttu-id="6de87-110">Gibt alle eindeutigen Eigenschaftswerte im Satz zurück, die für Zwecke wie das Anzeigen einer Familien Liste oder Tag Cloud verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6de87-110">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="6de87-111">Alle Werte werden unabhängig von der Sprache zurückgegeben, einschließlich aller lokalisierten Namen.</span><span class="sxs-lookup"><span data-stu-id="6de87-111">All values are returned regardless of language, including all localized names.</span></span> <br/>                                                                                       |
| <span data-ttu-id="6de87-112">[**GetPropertyValues (Eigenschaften-ID der dwrite- \_ Schriftart \_ , Konstante \_ WCHAR \* , idschreitestringlist \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="6de87-112">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, const WCHAR\*, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span></span>        | <span data-ttu-id="6de87-113">Gibt alle eindeutigen Eigenschaftswerte im Satz zurück, die für Zwecke wie das Anzeigen einer Familien Liste oder Tag Cloud verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6de87-113">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="6de87-114">Werte werden in der Reihenfolge ihrer Priorität entsprechend der Sprachliste zurückgegeben. Wenn eine Schriftart mehr als einen lokalisierten Namen enthält, wird der bevorzugte Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6de87-114">Values are returned in priority order according to the language list, such that if a font contains more than one localized name, the preferred one will be returned.</span></span> <br/> |
| <span data-ttu-id="6de87-115">[**GetPropertyValues (UInt32, dwrite \_ Font \_ Property \_ ID, bool \* , idschreitelocalizedstrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="6de87-115">[**GetPropertyValues(UINT32, DWRITE\_FONT\_PROPERTY\_ID, BOOL\*, IDWriteLocalizedStrings\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span> | <span data-ttu-id="6de87-116">Gibt die Eigenschaftswerte eines bestimmten Schriftart Element Indexes zurück.</span><span class="sxs-lookup"><span data-stu-id="6de87-116">Returns the property values of a specific font item index.</span></span><br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="6de87-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6de87-117">Requirements</span></span>



| <span data-ttu-id="6de87-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6de87-118">Requirement</span></span> | <span data-ttu-id="6de87-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6de87-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6de87-120">Header</span><span class="sxs-lookup"><span data-stu-id="6de87-120">Header</span></span><br/> | <dl> <span data-ttu-id="6de87-121"><dt>Dwrite \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="6de87-121"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de87-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6de87-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de87-123">**Idschreitefontset**</span><span class="sxs-lookup"><span data-stu-id="6de87-123">**IDWriteFontSet**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

<span data-ttu-id="6de87-124">�</span><span class="sxs-lookup"><span data-stu-id="6de87-124">�</span></span>

<span data-ttu-id="6de87-125">�</span><span class="sxs-lookup"><span data-stu-id="6de87-125">�</span></span>
