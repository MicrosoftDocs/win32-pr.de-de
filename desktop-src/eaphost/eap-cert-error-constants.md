---
title: EAP- \_ CERT-Fehler Konstanten (EAPHost RoR. h)
description: Definieren von Zertifikat bezogenen Fehlern, die allen EAPHost-API-Technologien gemeinsam sind.
ms.assetid: 12f626e1-520a-4aba-954b-769c3062a38c
topic_type:
- apiref
api_name:
- _EAP_CERT_FIRST
- _EAP_CERT_LAST
- _EAP_CERT_NOT_FOUND
- _EAP_CERT_INVALID
- _EAP_CERT_EXPIRED
- _EAP_CERT_REVOKED
- _EAP_CERT_OTHER_ERROR
- _EAP_CERT_REJECTED
- _EAP_CERT_NAME_REQUIRED
- _EAP_GENERAL_FIRST
- _EAP_GENERAL_LAST
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0543636f36d823b5557ad2f5a5f7cb000d93259a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517516"
---
# <a name="eap_cert-error-constants"></a>EAP- \_ CERT-Fehler Konstanten

Diese Konstanten definieren Zertifikat bezogene Fehler, die allen EAPHost-API-Technologien gemeinsam sind.

<dl> <dt>

<span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_EAP- \_ Zertifikat \_ zuerst**
</dt> <dd> <dl> <dt>

0x0
</dt> <dt>



Definiert die Grenze von Fehlerberichten. ein beliebiger Zertifikat Fehler tritt zwischen dem **\_ EAP-Zertifikat \_ \_ zuerst** und dem **\_ EAP \_ \_**-Zertifikat auf.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_EAP- \_ Zertifikat \_ zuletzt**
</dt> <dd> <dl> <dt>

0xF
</dt> <dt>



Definiert die Grenze von Fehlerberichten. ein beliebiger Zertifikat Fehler tritt zwischen dem **\_ EAP-Zertifikat \_ \_ zuerst** und dem **\_ EAP \_ \_**-Zertifikat auf.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_EAP- \_ Zertifikat wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Es wurde kein Benutzerzertifikat gefunden.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_EAP- \_ Zertifikat \_ ungültig**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Das Benutzerzertifikat ist ungültig.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_EAP- \_ Zertifikat \_ abgelaufen**
</dt> <dd> <dl> <dt>

0x3
</dt> <dt>



Das Benutzerzertifikat ist abgelaufen.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_EAP- \_ Zertifikat gesperrt \_**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



Das Benutzerzertifikat wurde widerrufen.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_anderer EAP- \_ CERT- \_ \_ Fehler**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



Unbekannter Zertifikat bezogener Fehler.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_EAP- \_ Zertifikat \_ abgelehnt**
</dt> <dd> <dl> <dt>

0x6
</dt> <dt>



Das Benutzerzertifikat wurde zurückgewiesen.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_EAP- \_ Zertifikat \_ Name \_ erforderlich**
</dt> <dd> <dl> <dt>

0x7
</dt> <dt>



Das Benutzerzertifikat erfordert einen Namen.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP ( \_ Allgemein) \_ zuerst**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Definiert die Grenze von Fehlerberichten. alle allgemeinen EAP-Fehler treten zwischen **\_ EAP \_ General \_ First** und **\_ EAP \_ General \_ Last** auf.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP \_ Allgemein (allgemein) \_**
</dt> <dd> <dl> <dt>

0x3F
</dt> <dt>



Definiert die Grenze von Fehlerberichten. alle allgemeinen EAP-Fehler treten zwischen **\_ EAP \_ General \_ First** und **\_ EAP \_ General \_ Last** auf.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                      |
| Header<br/>                   | <dl> <dt>EAPHost RoR. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine EAPHost-Konstanten](common-eap-host-error-constants.md)
</dt> </dl>

 

 





