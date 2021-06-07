---
title: Erweiterte Stile des ComboBoxEx-Steuerelements (CommCtrl.h)
description: Unterstützt die erweiterten Stile, die in diesem Abschnitt aufgeführt sind, sowie die meisten standard-Kombinationsfeld-Steuerelementstile.
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
ms.openlocfilehash: 966d259cf427bcc83e9a8b2fb65670a2a05b9458
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387656"
---
# <a name="comboboxex-control-extended-styles"></a><span data-ttu-id="60373-103">Erweiterte Stile des ComboBoxEx-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="60373-103">ComboBoxEx Control Extended Styles</span></span>

<span data-ttu-id="60373-104">Unterstützt die erweiterten Stile, die in diesem Abschnitt aufgeführt sind, sowie die meisten standard-Kombinationsfeld-Steuerelementstile.</span><span class="sxs-lookup"><span data-stu-id="60373-104">Support the extended styles that are listed in this section as well as most standard combo box control styles.</span></span>



| <span data-ttu-id="60373-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="60373-105">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="60373-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60373-106">Description</span></span>                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <span data-ttu-id="60373-107"><dt>**CBES \_ OHNE \_ SENSITIVE GROß-/KLEINSCHREIBUNG**</dt></span><span class="sxs-lookup"><span data-stu-id="60373-107"><dt>**CBES\_EX\_CASESENSITIVE**</dt></span></span> </dl>             | <span data-ttu-id="60373-108">Bei **BSTR-Suchen** in der Liste wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="60373-108">**BSTR** searches in the list will be case sensitive.</span></span> <span data-ttu-id="60373-109">Dies schließt Suchvorgänge als Ergebnis der Eingabe von Text in das Bearbeitungsfeld und die CB \_ FINDSTRINGEXACT-Nachricht ein.</span><span class="sxs-lookup"><span data-stu-id="60373-109">This includes searches as a result of text being typed in the edit box and the CB\_FINDSTRINGEXACT message.</span></span><br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <span data-ttu-id="60373-110"><dt>**CBES \_ EX \_ NOEDITIMAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="60373-110"><dt>**CBES\_EX\_NOEDITIMAGE**</dt></span></span> </dl>                   | <span data-ttu-id="60373-111">Im Bearbeitungsfeld und in der Dropdownliste werden keine Elementbilder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="60373-111">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <span data-ttu-id="60373-112"><dt>**CBES \_ EX \_ NOEDITIMAGEINDENT**</dt></span><span class="sxs-lookup"><span data-stu-id="60373-112"><dt>**CBES\_EX\_NOEDITIMAGEINDENT**</dt></span></span> </dl> | <span data-ttu-id="60373-113">Im Bearbeitungsfeld und in der Dropdownliste werden keine Elementbilder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="60373-113">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <span data-ttu-id="60373-114"><dt>**CBES \_ EX \_ NOSIZELIMIT**</dt></span><span class="sxs-lookup"><span data-stu-id="60373-114"><dt>**CBES\_EX\_NOSIZELIMIT**</dt></span></span> </dl>                   | <span data-ttu-id="60373-115">Ermöglicht, dass das ComboBoxEx-Steuerelement vertikal kleiner als das enthaltene Kombinationsfeld-Steuerelement ist.</span><span class="sxs-lookup"><span data-stu-id="60373-115">Allows the ComboBoxEx control to be vertically sized smaller than its contained combo box control.</span></span> <span data-ttu-id="60373-116">Wenn comboBoxEx kleiner als das Kombinationsfeld ist, wird das Kombinationsfeld abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="60373-116">If the ComboBoxEx is sized smaller than the combo box, the combo box will be clipped.</span></span> <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <span data-ttu-id="60373-117"><dt>**CBES \_ EX \_ PATHWORDBREAKPROC**</dt></span><span class="sxs-lookup"><span data-stu-id="60373-117"><dt>**CBES\_EX\_PATHWORDBREAKPROC**</dt></span></span> </dl> | <span data-ttu-id="60373-118">Nur Windows NT.</span><span class="sxs-lookup"><span data-stu-id="60373-118">Windows NT only.</span></span> <span data-ttu-id="60373-119">Im Bearbeitungsfeld werden der Schrägstrich (/), der umgekehrte Schrägstrich \\ () und der Punkt (.) als Worttrennzeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="60373-119">The edit box will use the slash (/), backslash (\\), and period (.) characters as word delimiters.</span></span> <span data-ttu-id="60373-120">Dadurch sind Tastenkombinationen für die Cursorbewegung von Wort zu Wort in Pfadnamen und URLs effektiv.</span><span class="sxs-lookup"><span data-stu-id="60373-120">This makes keyboard shortcuts for word-by-word cursor movement effective in path names and URLs.</span></span><br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <span data-ttu-id="60373-121"><dt>**CBES \_ EX \_ TEXTENDELLIPSIS**</dt></span><span class="sxs-lookup"><span data-stu-id="60373-121"><dt>**CBES\_EX\_TEXTENDELLIPSIS**</dt></span></span> </dl>       | <span data-ttu-id="60373-122">**Windows Vista und höher.**</span><span class="sxs-lookup"><span data-stu-id="60373-122">**Windows Vista and later.**</span></span> <span data-ttu-id="60373-123">Bewirkt, dass Elemente in der Dropdownliste und im Bearbeitungsfeld (wenn das Bearbeitungsfeld schreibgeschützt ist) mit einem Auslassungszeichen ("...") abgeschnitten werden, anstatt nur vom Rand des Steuerelements abgeschnitten zu werden.</span><span class="sxs-lookup"><span data-stu-id="60373-123">Causes items in the drop-down list and the edit box (when the edit box is read only) to be truncated with an ellipsis ("...") rather than just clipped by the edge of the control.</span></span> <span data-ttu-id="60373-124">Dies ist nützlich, wenn das Steuerelement auf eine feste Breite festgelegt werden muss, die Einträge in der Liste jedoch möglicherweise lang sind.</span><span class="sxs-lookup"><span data-stu-id="60373-124">This is useful when the control needs to be set to a fixed width, yet the entries in the list may be long.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="60373-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="60373-125">Remarks</span></span>

<span data-ttu-id="60373-126">Sie können die erweiterten Stile des Kombinationsfelds mithilfe von [**CBEM \_ SETEXTENDEDSTYLE-**](cbem-setextendedstyle.md) und [**CBEM \_ GETEXTENDEDSTYLE-Nachrichten**](cbem-getextendedstyle.md) festlegen und abrufen.</span><span class="sxs-lookup"><span data-stu-id="60373-126">You set and retrieve the combobox extended styles by using [**CBEM\_SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) and [**CBEM\_GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="60373-127">Wenn Sie versuchen, einen erweiterten Stil für ein ComboBoxEx-Steuerelement festzulegen, das mit dem [**CBS \_ SIMPLE-Stil**](combo-box-styles.md) erstellt wurde, wird es möglicherweise nicht ordnungsgemäß neu zusammengestellt.</span><span class="sxs-lookup"><span data-stu-id="60373-127">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it might not repaint properly.</span></span> <span data-ttu-id="60373-128">Der **CBS \_ SIMPLE-Stil** funktioniert auch nicht ordnungsgemäß mit dem erweiterten CBES \_ EX \_ PATHWORDBREAKPROC-Stil.</span><span class="sxs-lookup"><span data-stu-id="60373-128">The **CBS\_SIMPLE** style also does not work properly with the CBES\_EX\_PATHWORDBREAKPROC extended style.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="60373-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="60373-129">Requirements</span></span>



| <span data-ttu-id="60373-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60373-130">Requirement</span></span> | <span data-ttu-id="60373-131">Wert</span><span class="sxs-lookup"><span data-stu-id="60373-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60373-132">Header</span><span class="sxs-lookup"><span data-stu-id="60373-132">Header</span></span><br/> | <dl> <span data-ttu-id="60373-133"><dt>CommCtrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="60373-133"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





