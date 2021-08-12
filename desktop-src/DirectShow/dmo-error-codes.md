---
description: Die folgende Tabelle enthält Fehlercodes, die spezifisch für Microsoft DirectX Media Objects (DMOs) sind. Diese Fehlercodes werden in der Headerdatei Mediaerr.h definiert.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: DMO Fehlercodes (Mediaerr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa8f45b8f9f61185adbcd79a354df8ab3e41471067b66179193b825a5e40651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653294"
---
# <a name="dmo-error-codes"></a>DMO Fehlercodes

Die folgende Tabelle enthält Fehlercodes, die spezifisch für Microsoft DirectX Media Objects (DMOs) sind. Diese Fehlercodes werden in der Headerdatei Mediaerr.h definiert.



| Konstante/Wert                                                                                                                                                                                                                                                  | Beschreibung                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <dt>**DMO \_ E \_ INVALIDSTREAMINDEX-0x80040201**</dt> <dt></dt> </dl> | Ungültiger Streamindex.<br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <dt>**DMO \_ E \_ INVALIDTYPE-0x80040202**</dt> <dt></dt> </dl>                      | Ungültiger Medientyp.<br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <dt>**DMO \_ E \_ TYPE \_ NOT \_ SET**</dt> <dt>0x80040203</dt> </dl>                 | Der Medientyp wurde nicht festgelegt. Mindestens ein Datenstrom erfordert einen Medientyp, bevor dieser Vorgang ausgeführt werden kann.<br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <dt>**DMO \_ E \_ NOTACCEPTING**</dt> <dt>0x80040204</dt> </dl>                   | Daten können in diesem Stream nicht akzeptiert werden. Möglicherweise müssen Sie weitere Ausgabedaten verarbeiten. siehe [**IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).<br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <dt>**DMO \_ E \_ TYPE NOT ACCEPTED \_ \_ 0X80040205**</dt> <dt></dt> </dl>  | Der Medientyp wurde nicht akzeptiert.<br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <dt>**DMO \_ E \_ KEINE ELEMENTE MEHR \_ \_ 0X80040206**</dt> <dt></dt> </dl>              | Der Medientypindex liegt nicht im Bereich.<br/>                                                                                                                        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mediaerr.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DMO Konstanten](dmo-constants.md)
</dt> </dl>

 

 




