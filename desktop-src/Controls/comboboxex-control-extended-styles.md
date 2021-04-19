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
# <a name="comboboxex-control-extended-styles"></a>Erweiterte Stile des ComboBoxEx-Steuer Elements

Unterstützen Sie die erweiterten Stile, die in diesem Abschnitt aufgeführt sind, sowie die meisten Standardformate für Kombinations Feld-Steuerelemente.



| Konstante                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <dt>**CBEs \_ Ex \_ CaseSensitive**</dt> </dl>             | Bei **BSTR** -suchen in der Liste wird Groß-/Kleinschreibung beachtet. Dies schließt Suchvorgänge als Ergebnis des eingegebenen Texts in das Eingabefeld und die CB- \_ FindStringExact-Nachricht ein.<br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <dt>**CBEs \_ Ex \_ noeditimage**</dt> </dl>                   | Im Bearbeitungsfeld und in der Dropdown Liste werden keine Element Bilder angezeigt. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <dt>**CBEs \_ " \_ noeditimagein Dent"**</dt> </dl> | Im Bearbeitungsfeld und in der Dropdown Liste werden keine Element Bilder angezeigt. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <dt>**CBEs \_ Ex \_ nosizelimit**</dt> </dl>                   | Ermöglicht die vertikale Größe des Steuer Elements ComboBoxEx, das kleiner als das enthaltene Kombinations Feld-Steuerelement ist. Wenn die Größe von ComboBoxEx kleiner als das Kombinations Feld ist, wird das Kombinations Feld abgeschnitten. <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <dt>**CBEs \_ Ex \_ pathwordbreakproc**</dt> </dl> | Nur Windows NT. Im Bearbeitungsfeld werden die Zeichen Schrägstrich (/), umgekehrter Schrägstrich ( \) und Punkte (.) als Wort Trennzeichen verwendet. Dies bewirkt, dass Tastenkombinationen für die Wort gesteuerte Cursor Bewegung in Pfadnamen und URLs wirksam werden.<br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <dt>**CBEs \_ Ex \_ textendellipsis**</dt> </dl>       | **Windows Vista und höher.** Bewirkt, dass Elemente in der Dropdown Liste und im Bearbeitungsfeld (wenn das Bearbeitungsfeld schreibgeschützt ist) mit einem Auslassungs Zeichen ("...") abgeschnitten werden, anstatt einfach durch den Rand des Steuer Elements abgeschnitten zu werden. Dies ist hilfreich, wenn das Steuerelement auf eine festgelegte Breite festgelegt werden muss, die Einträge in der Liste jedoch möglicherweise lang sind.<br/> |



## <a name="remarks"></a>Bemerkungen

Mithilfe von [**CBEM \_ SetExtendedStyle**](cbem-setextendedstyle.md) -und [**CBEM \_ GetExtendedStyle**](cbem-getextendedstyle.md) -Meldungen werden erweiterte Stile für ComboBox festgelegt und abgerufen.

> [!Note]  
> Wenn Sie versuchen, einen erweiterten Stil für ein ComboBoxEx-Steuerelement festzulegen, das mit dem [**\_ einfachen CBS**](combo-box-styles.md) -Stil erstellt wurde, wird es möglicherweise nicht ordnungsgemäß neu gezeichnet. Der **\_ einfache CBS** -Stil funktioniert auch nicht ordnungsgemäß mit dem erweiterten Format CBEs \_ Ex \_ pathwordbreakproc.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





