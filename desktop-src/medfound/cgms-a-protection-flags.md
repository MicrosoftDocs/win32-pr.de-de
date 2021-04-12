---
description: Geben Sie die Schutz Ebenen für das Verwaltungs System für die Kopier Generierung an&\# 8212; Analog (CGMS-A).
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: CGMS-A-Schutzflags (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329ae13741490f2783d548baeead65ba59bc5ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393306"
---
# <a name="cgms-a-protection-flags"></a>CGMS-A-Schutzflags

In den Konstanten in der folgenden Tabelle sind die Schutz Ebenen für die analog zum Management System für Kopier Generierung (CGMS-A) angegeben.



| Konstante/Wert                                                                                                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <dt>**OPM \_ Cgmsa \_ außerhalb von**</dt> <dt>0x00</dt> </dl>                                                                                       | CGMS-A ist deaktiviert. <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <dt>**OPM \_ Cgmsa- \_ Kopie \_ frei**</dt> <dt>0x01</dt> </dl>                                                              | Die Schutz Ebene ist kostenlos kopieren.<br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <dt>**OPM \_ Cgmsa- \_ Kopie \_ nicht \_ mehr**</dt> <dt>0x02</dt> </dl>                                                          | Die Schutz Ebene ist "Kopieren". <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <dt>**OPM \_ Cgmsa \_ Kopie \_ 1 \_ Generation**</dt> <dt>0x03</dt> </dl>                                     | Die Schutz Ebene ist Kopie einer Generation. <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <dt>**OPM \_ Cgmsa- \_ Kopie \_ nie**</dt> <dt>0x04</dt> </dl>                                                                 | Die Schutz Ebene ist nie kopieren.<br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <dt>**OPM \_ Cgmsa \_ - \_ weitergabesteuerelement \_ erforderlich**</dt> <dt>0x08</dt> </dl> | Ein weitergabesteuerelement (auch als *Broadcast-Flag* bezeichnet) ist erforderlich. Dieses Flag kann mit den anderen Flags kombiniert werden.<br/> |



## <a name="remarks"></a>Bemerkungen

Diese Flags entsprechen den Enumerationskonstanten der **COPP \_ cgmsa- \_ Schutz \_ Ebene** , die im Certified Output Protection Protocol (COPP) verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Konstanten](media-foundation-constants.md)
</dt> </dl>

 

 




