---
title: Erweiterte Stile des ComboBoxEx-Steuer Elements (kommctrl. h)
description: Unterstützen Sie die erweiterten Stile, die in diesem Abschnitt aufgeführt sind, sowie die meisten Standardformate für Kombinations Feld-Steuerelemente.
ms.assetid: 4741ac5e-1c46-4fd3-9174-b4ceb479261f
topic_type:
- apiref
api_name:
- CBES_EX_CASESENSITIVE
- CBES_EX_NOEDITIMAGE
- CBES_EX_NOEDITIMAGEINDENT
- CBES_EX_NOSIZELIMIT
- CBES_EX_PATHWORDBREAKPROC
- CBES_EX_TEXTENDELLIPSIS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71dc92264dbd1bd2f5a4b1136d9a6138e1fcffa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370672"
---
# <a name="comboboxex-control-extended-styles"></a><span data-ttu-id="3b11d-103">Erweiterte Stile des ComboBoxEx-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="3b11d-103">ComboBoxEx Control Extended Styles</span></span>

<span data-ttu-id="3b11d-104">Unterstützen Sie die erweiterten Stile, die in diesem Abschnitt aufgeführt sind, sowie die meisten Standardformate für Kombinations Feld-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="3b11d-104">Support the extended styles that are listed in this section as well as most standard combo box control styles.</span></span>



| <span data-ttu-id="3b11d-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="3b11d-105">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="3b11d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b11d-106">Description</span></span>                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <span data-ttu-id="3b11d-107"><dt>**CBEs \_ Ex \_ CaseSensitive**</dt></span><span class="sxs-lookup"><span data-stu-id="3b11d-107"><dt>**CBES\_EX\_CASESENSITIVE**</dt></span></span> </dl>             | <span data-ttu-id="3b11d-108">Bei **BSTR** -suchen in der Liste wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="3b11d-108">**BSTR** searches in the list will be case sensitive.</span></span> <span data-ttu-id="3b11d-109">Dies schließt Suchvorgänge als Ergebnis des eingegebenen Texts in das Eingabefeld und die CB- \_ FindStringExact-Nachricht ein.</span><span class="sxs-lookup"><span data-stu-id="3b11d-109">This includes searches as a result of text being typed in the edit box and the CB\_FINDSTRINGEXACT message.</span></span><br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <span data-ttu-id="3b11d-110"><dt>**CBEs \_ Ex \_ noeditimage**</dt></span><span class="sxs-lookup"><span data-stu-id="3b11d-110"><dt>**CBES\_EX\_NOEDITIMAGE**</dt></span></span> </dl>                   | <span data-ttu-id="3b11d-111">Im Bearbeitungsfeld und in der Dropdown Liste werden keine Element Bilder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3b11d-111">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <span data-ttu-id="3b11d-112"><dt>**CBEs \_ " \_ noeditimagein Dent"**</dt></span><span class="sxs-lookup"><span data-stu-id="3b11d-112"><dt>**CBES\_EX\_NOEDITIMAGEINDENT**</dt></span></span> </dl> | <span data-ttu-id="3b11d-113">Im Bearbeitungsfeld und in der Dropdown Liste werden keine Element Bilder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3b11d-113">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <span data-ttu-id="3b11d-114"><dt>**CBEs \_ Ex \_ nosizelimit**</dt></span><span class="sxs-lookup"><span data-stu-id="3b11d-114"><dt>**CBES\_EX\_NOSIZELIMIT**</dt></span></span> </dl>                   | <span data-ttu-id="3b11d-115">Ermöglicht die vertikale Größe des Steuer Elements ComboBoxEx, das kleiner als das enthaltene Kombinations Feld-Steuerelement ist.</span><span class="sxs-lookup"><span data-stu-id="3b11d-115">Allows the ComboBoxEx control to be vertically sized smaller than its contained combo box control.</span></span> <span data-ttu-id="3b11d-116">Wenn die Größe von ComboBoxEx kleiner als das Kombinations Feld ist, wird das Kombinations Feld abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="3b11d-116">If the ComboBoxEx is sized smaller than the combo box, the combo box will be clipped.</span></span> <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <span data-ttu-id="3b11d-117"><dt>**CBEs \_ Ex \_ pathwordbreakproc**</dt></span><span class="sxs-lookup"><span data-stu-id="3b11d-117"><dt>**CBES\_EX\_PATHWORDBREAKPROC**</dt></span></span> </dl> | <span data-ttu-id="3b11d-118">Nur Windows NT.</span><span class="sxs-lookup"><span data-stu-id="3b11d-118">Windows NT only.</span></span> <span data-ttu-id="3b11d-119">Im Bearbeitungsfeld werden die Zeichen Schrägstrich (/), umgekehrter Schrägstrich ( \) und Punkte (.) als Wort Trennzeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b11d-119">The edit box will use the slash (/), backslash (\), and period (.) characters as word delimiters.</span></span> <span data-ttu-id="3b11d-120">Dies bewirkt, dass Tastenkombinationen für die Wort gesteuerte Cursor Bewegung in Pfadnamen und URLs wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="3b11d-120">This makes keyboard shortcuts for word-by-word cursor movement effective in path names and URLs.</span></span><br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <span data-ttu-id="3b11d-121"><dt>**CBEs \_ Ex \_ textendellipsis**</dt></span><span class="sxs-lookup"><span data-stu-id="3b11d-121"><dt>**CBES\_EX\_TEXTENDELLIPSIS**</dt></span></span> </dl>       | <span data-ttu-id="3b11d-122">**Windows Vista und höher.**</span><span class="sxs-lookup"><span data-stu-id="3b11d-122">**Windows Vista and later.**</span></span> <span data-ttu-id="3b11d-123">Bewirkt, dass Elemente in der Dropdown Liste und im Bearbeitungsfeld (wenn das Bearbeitungsfeld schreibgeschützt ist) mit einem Auslassungs Zeichen ("...") abgeschnitten werden, anstatt einfach durch den Rand des Steuer Elements abgeschnitten zu werden.</span><span class="sxs-lookup"><span data-stu-id="3b11d-123">Causes items in the drop-down list and the edit box (when the edit box is read only) to be truncated with an ellipsis ("...") rather than just clipped by the edge of the control.</span></span> <span data-ttu-id="3b11d-124">Dies ist hilfreich, wenn das Steuerelement auf eine festgelegte Breite festgelegt werden muss, die Einträge in der Liste jedoch möglicherweise lang sind.</span><span class="sxs-lookup"><span data-stu-id="3b11d-124">This is useful when the control needs to be set to a fixed width, yet the entries in the list may be long.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3b11d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b11d-125">Remarks</span></span>

<span data-ttu-id="3b11d-126">Mithilfe von [**CBEM \_ SetExtendedStyle**](cbem-setextendedstyle.md) -und [**CBEM \_ GetExtendedStyle**](cbem-getextendedstyle.md) -Meldungen werden erweiterte Stile für ComboBox festgelegt und abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3b11d-126">You set and retrieve the combobox extended styles by using [**CBEM\_SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) and [**CBEM\_GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="3b11d-127">Wenn Sie versuchen, einen erweiterten Stil für ein ComboBoxEx-Steuerelement festzulegen, das mit dem [**\_ einfachen CBS**](combo-box-styles.md) -Stil erstellt wurde, wird es möglicherweise nicht ordnungsgemäß neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3b11d-127">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it might not repaint properly.</span></span> <span data-ttu-id="3b11d-128">Der **\_ einfache CBS** -Stil funktioniert auch nicht ordnungsgemäß mit dem erweiterten Format CBEs \_ Ex \_ pathwordbreakproc.</span><span class="sxs-lookup"><span data-stu-id="3b11d-128">The **CBS\_SIMPLE** style also does not work properly with the CBES\_EX\_PATHWORDBREAKPROC extended style.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3b11d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b11d-129">Requirements</span></span>



| <span data-ttu-id="3b11d-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b11d-130">Requirement</span></span> | <span data-ttu-id="3b11d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="3b11d-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b11d-132">Header</span><span class="sxs-lookup"><span data-stu-id="3b11d-132">Header</span></span><br/> | <dl> <span data-ttu-id="3b11d-133"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b11d-133"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





