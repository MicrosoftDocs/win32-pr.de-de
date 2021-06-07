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
# <a name="comboboxex-control-extended-styles"></a>Erweiterte Stile des ComboBoxEx-Steuerelements

Unterstützt die erweiterten Stile, die in diesem Abschnitt aufgeführt sind, sowie die meisten standard-Kombinationsfeld-Steuerelementstile.



| Konstante                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <dt>**CBES \_ OHNE \_ SENSITIVE GROß-/KLEINSCHREIBUNG**</dt> </dl>             | Bei **BSTR-Suchen** in der Liste wird die Groß-/Kleinschreibung beachtet. Dies schließt Suchvorgänge als Ergebnis der Eingabe von Text in das Bearbeitungsfeld und die CB \_ FINDSTRINGEXACT-Nachricht ein.<br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <dt>**CBES \_ EX \_ NOEDITIMAGE**</dt> </dl>                   | Im Bearbeitungsfeld und in der Dropdownliste werden keine Elementbilder angezeigt. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <dt>**CBES \_ EX \_ NOEDITIMAGEINDENT**</dt> </dl> | Im Bearbeitungsfeld und in der Dropdownliste werden keine Elementbilder angezeigt. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <dt>**CBES \_ EX \_ NOSIZELIMIT**</dt> </dl>                   | Ermöglicht, dass das ComboBoxEx-Steuerelement vertikal kleiner als das enthaltene Kombinationsfeld-Steuerelement ist. Wenn comboBoxEx kleiner als das Kombinationsfeld ist, wird das Kombinationsfeld abgeschnitten. <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <dt>**CBES \_ EX \_ PATHWORDBREAKPROC**</dt> </dl> | Nur Windows NT. Im Bearbeitungsfeld werden der Schrägstrich (/), der umgekehrte Schrägstrich \\ () und der Punkt (.) als Worttrennzeichen verwendet. Dadurch sind Tastenkombinationen für die Cursorbewegung von Wort zu Wort in Pfadnamen und URLs effektiv.<br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <dt>**CBES \_ EX \_ TEXTENDELLIPSIS**</dt> </dl>       | **Windows Vista und höher.** Bewirkt, dass Elemente in der Dropdownliste und im Bearbeitungsfeld (wenn das Bearbeitungsfeld schreibgeschützt ist) mit einem Auslassungszeichen ("...") abgeschnitten werden, anstatt nur vom Rand des Steuerelements abgeschnitten zu werden. Dies ist nützlich, wenn das Steuerelement auf eine feste Breite festgelegt werden muss, die Einträge in der Liste jedoch möglicherweise lang sind.<br/> |



## <a name="remarks"></a>Hinweise

Sie können die erweiterten Stile des Kombinationsfelds mithilfe von [**CBEM \_ SETEXTENDEDSTYLE-**](cbem-setextendedstyle.md) und [**CBEM \_ GETEXTENDEDSTYLE-Nachrichten**](cbem-getextendedstyle.md) festlegen und abrufen.

> [!Note]  
> Wenn Sie versuchen, einen erweiterten Stil für ein ComboBoxEx-Steuerelement festzulegen, das mit dem [**CBS \_ SIMPLE-Stil**](combo-box-styles.md) erstellt wurde, wird es möglicherweise nicht ordnungsgemäß neu zusammengestellt. Der **CBS \_ SIMPLE-Stil** funktioniert auch nicht ordnungsgemäß mit dem erweiterten CBES \_ EX \_ PATHWORDBREAKPROC-Stil.

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





