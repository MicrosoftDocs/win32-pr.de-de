---
description: In der folgenden Tabelle sind die für Microsoft DirectX Media Objects (DMOs) spezifischen Fehlercodes enthalten. Diese Fehlercodes sind in der Header Datei mediaerr. h definiert.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: DMO-Fehler Codes (mediaerr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365797"
---
# <a name="dmo-error-codes"></a>DMO-Fehler Codes

In der folgenden Tabelle sind die für Microsoft DirectX Media Objects (DMOs) spezifischen Fehlercodes enthalten. Diese Fehlercodes sind in der Header Datei mediaerr. h definiert.



| Konstante/Wert                                                                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <dt>**DMO \_ E \_ invalidstreamindex**</dt> <dt>0x80040201</dt> </dl> | Ungültiger streamindex.<br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <dt>**DMO \_ E \_ invalidtype**</dt> <dt>0x80040202</dt> </dl>                      | Ungültiger Medientyp.<br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <dt>**DMO \_ E- \_ Typ \_ nicht \_ festgelegt**</dt> <dt>0x80040203</dt> </dl>                 | Der Medientyp wurde nicht festgelegt. Mindestens ein Stream erfordert einen Medientyp, bevor dieser Vorgang ausgeführt werden kann.<br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <dt>**DMO \_ E nicht \_ akzeptieren**</dt> <dt>0x80040204</dt> </dl>                   | Daten können für diesen Datenstrom nicht akzeptiert werden. Möglicherweise müssen Sie mehr Ausgabedaten verarbeiten. Weitere Informationen finden Sie unter [**imediaobject::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).<br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <dt>**DMO \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt> <dt>0x80040205</dt> </dl>  | Der Medientyp wurde nicht akzeptiert.<br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <dt>**DMO \_ E \_ keine \_ weiteren \_ Elemente**</dt> <dt>0x80040206</dt> </dl>              | Der Medientyp Index liegt außerhalb des zulässigen Bereichs.<br/>                                                                                                                        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Mediaerr. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DMO-Konstanten](dmo-constants.md)
</dt> </dl>

 

 




