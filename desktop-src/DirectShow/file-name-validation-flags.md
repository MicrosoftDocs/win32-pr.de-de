---
description: Diese Flags geben das Verhalten des Medienlocator an.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Validierungsflags für Dateinamen (Qedit.h)
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
ms.openlocfilehash: 44bbeebc344edf1c6a9c5a5d287bea7cdfe87e96d9af09a65417411d6cd43820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015768"
---
# <a name="file-name-validation-flags"></a>Validierungsflags für Dateinamen

\[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

Diese Flags geben das Verhalten des Medienlocator an.



| Konstante/Wert                                                                                                                                                                                                                                               | Beschreibung                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <dt>**SFN \_ VALIDATEF \_ CHECK**</dt> <dt>0x01</dt> </dl>                   | Überprüfen Sie die Gültigkeit von Dateinamen. Sie müssen dieses Flag festlegen, um Dateinamen zu überprüfen. Wenn dies nicht der Dert ist, haben die anderen Flags keine Auswirkungen.<br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <dt>**SFN \_ VALIDATEF \_ POPUP**</dt> <dt>0x02</dt> </dl>                   | Wenn keine Datei gefunden wird, zeigen Sie ein Dialogfeld Datei öffnen für den Endbenutzer an.<br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <dt>**SFN \_ VALIDATEF \_ TELLME**</dt> <dt>0x04</dt> </dl>                | Wenn eine fehlende Datei gefunden wird, zeigen Sie kurz ein Meldungsfeld mit dem Namen und Speicherort der Datei an. Dieses Flag ist hauptsächlich für Testzwecke nützlich. das Meldungsfeld ist wahrscheinlich nicht für ein Einzelhandelsprodukt geeignet.<br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <dt>**SFN \_ VALIDATEF \_ REPLACE**</dt> <dt>0x08</dt> </dl>             | Wenn eine fehlende Datei gefunden wird, aktualisieren Sie den Namen des Quellobjekts. (Nur gültig in der [**IAMTimeline::ValidateSourceNames-Methode.)**](iamtimeline-validatesourcenames.md)<br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <dt>**SFN \_ VALIDATEF \_ USELOCAL**</dt> <dt>0x10</dt> </dl>          | Verwenden Sie immer eine lokale Datei, auch wenn eine Version der Datei im Netzwerk vorhanden ist.<br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <dt>**SFN \_ VALIDATEF \_ NOFIND-0x20**</dt> <dt></dt> </dl>                | Suchen Sie nicht nach fehlenden Dateien. Dateinamen werden weiterhin überprüft, wenn Sie das SFN \_ VALIDATEF \_ CHECK-Flag festlegen.<br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <dt>**SFN \_ VALIDATEF \_ IGNOREMUTED**</dt> <dt>0x40</dt> </dl> | Ignoriert mutierte Quellobjekte. (Nur gültig in der [**IAMTimeline::ValidateSourceNames-Methode.)**](iamtimeline-validatesourcenames.md)<br/>                                                                                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md)
</dt> <dt>

[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




