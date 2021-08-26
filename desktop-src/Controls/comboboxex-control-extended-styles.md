---
title: ComboBoxEx-Steuerelement erweiterte Stile (CommCtrl.h)
description: Unterstützen Sie die erweiterten Stile, die in diesem Abschnitt aufgeführt sind, sowie die meisten standarden Kombinationsfeld-Steuerelementstile.
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
ms.openlocfilehash: aed3ca32fa063b9b824a2ecd444a6a71c1885697f839b67e117c75622f009c60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921150"
---
# <a name="comboboxex-control-extended-styles"></a>Erweiterte Stile des ComboBoxEx-Steuerelements

Unterstützen Sie die erweiterten Stile, die in diesem Abschnitt aufgeführt sind, sowie die meisten standarden Kombinationsfeld-Steuerelementstile.



| Konstante                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <dt>**CBES \_ EX \_ CASESENSITIVE**</dt> </dl>             | **Bei** BSTR-Suchvorgängen in der Liste wird die Kleinschreibung beachtet. Dies schließt Suchvorgänge als Ergebnis der Texttypierung in das Bearbeitungsfeld und die CB \_ FINDSTRINGEXACT-Nachricht ein.<br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <dt>**CBES \_ EX \_ NOEDITIMAGE**</dt> </dl>                   | Im Bearbeitungsfeld und in der Dropdownliste werden keine Elementbilder angezeigt. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <dt>**CBES \_ EX \_ NOEDITIMAGEINDENT**</dt> </dl> | Im Bearbeitungsfeld und in der Dropdownliste werden keine Elementbilder angezeigt. <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <dt>**CBES \_ EX \_ NOSIZELIMIT**</dt> </dl>                   | Ermöglicht es dem ComboBoxEx-Steuerelement, eine vertikale Größe zu haben, die kleiner ist als das enthaltene Kombinationsfeld-Steuerelement. Wenn comboBoxEx kleiner als das Kombinationsfeld ist, wird das Kombinationsfeld abgeschnitten. <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <dt>**CBES \_ EX \_ PATHWORDBREAKPROC**</dt> </dl> | Windows Nur NT. Im Bearbeitungsfeld werden die Schrägstriche (/), der schräge Schrägstrich () und der \\ Zeitraum (.) als Worttrennzeichen verwendet. Dadurch werden Tastenkombinationen für die Wort-für-Wort-Cursorbewegung in Pfadnamen und URLs wirksam.<br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <dt>**CBES \_ EX \_ TEXTENDELLIPSIS**</dt> </dl>       | **Windows Vista und höher.** Bewirkt, dass Elemente in der Dropdownliste und im Bearbeitungsfeld (wenn das Bearbeitungsfeld schreibgeschützt ist) nicht nur am Rand des Steuerelements abgeschnitten werden, sondern durch Auslassungspunkte ("..."). Dies ist nützlich, wenn das Steuerelement auf eine feste Breite festgelegt werden muss, die Einträge in der Liste jedoch möglicherweise lang sind.<br/> |



## <a name="remarks"></a>Hinweise

Sie können die erweiterten Stile des Kombinationsfelds mithilfe von [**CBEM \_ SETEXTENDEDSTYLE-**](cbem-setextendedstyle.md) und [**CBEM \_ GETEXTENDEDSTYLE-Nachrichten**](cbem-getextendedstyle.md) festlegen und abrufen.

> [!Note]  
> Wenn Sie versuchen, einen erweiterten Stil für ein ComboBoxEx-Steuerelement zu erstellen, das mit dem [**CBS \_ SIMPLE-Stil**](combo-box-styles.md) erstellt wurde, wird es möglicherweise nicht ordnungsgemäß neu gepaint. Der **CBS \_ SIMPLE-Stil** funktioniert auch nicht ordnungsgemäß mit dem erweiterten CBES \_ EX \_ PATHWORDBREAKPROC-Stil.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





