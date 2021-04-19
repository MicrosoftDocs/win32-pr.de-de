---
description: Diese Flags geben das Verhalten des medienlocators an.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Dateiname-Validierungsflags (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: d8930241be0306c637bcab36207fec1de2e489c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372039"
---
# <a name="file-name-validation-flags"></a>Dateiname-Überprüfung

\[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

Diese Flags geben das Verhalten des medienlocators an.



| Konstante/Wert                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <dt>**SFN \_ Validatef- \_ Überprüfung**</dt> <dt>0x01</dt> </dl>                   | Überprüfen Sie die Gültigkeit von Dateinamen. Sie müssen dieses Flag festlegen, um Dateinamen zu überprüfen. Andernfalls haben die anderen Flags keine Auswirkung.<br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <dt>**SFN \_ Validatef- \_ Popup**</dt> <dt>0x02</dt> </dl>                   | Wenn eine Datei nicht gefunden wird, können Sie das Dialogfeld Datei öffnen für den Endbenutzer anzeigen.<br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <dt>**SFN \_ Validatef- \_ Tellme**</dt> <dt>0x04</dt> </dl>                | Wenn eine fehlende Datei gefunden wird, zeigen Sie kurz ein Meldungs Feld mit dem Namen und dem Speicherort der Datei an. Dieses Flag ist hauptsächlich für Testzwecke nützlich. das Meldungs Feld eignet sich wahrscheinlich nicht für ein Einzelhandelsprodukt.<br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <dt>**SFN \_ Validatef \_ Replace**</dt> <dt>0x08</dt> </dl>             | Wenn eine fehlende Datei gefunden wird, aktualisieren Sie den Namen des Quell Objekts. (Nur gültig in der [**iamtimeline:: validatesourcenames**](iamtimeline-validatesourcenames.md) -Methode.)<br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <dt>**SFN \_ Validatef \_ uselocal**</dt> <dt>0x10</dt> </dl>          | Verwenden Sie immer eine lokale Datei, auch wenn eine Version der Datei im Netzwerk vorhanden ist.<br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <dt>**SFN \_ Validatef \_ NoFind**</dt> <dt>0x20</dt> </dl>                | Nicht nach fehlenden Dateien suchen. Dateinamen werden nach wie vor überprüft, wenn Sie das \_ Check-Flag SFN validatef festlegen \_ .<br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <dt>**SFN \_ Validatef \_ ignoremuted**</dt> <dt>0x40</dt> </dl> | Musterte Quell Objekte ignorieren. (Nur gültig in der [**iamtimeline:: validatesourcenames**](iamtimeline-validatesourcenames.md) -Methode.)<br/>                                                                                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>"Qedit. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imedialocator:: findmediafile**](imedialocator-findmediafile.md)
</dt> <dt>

[**"Unenderengine:: setsourcenamevalidation"**](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




