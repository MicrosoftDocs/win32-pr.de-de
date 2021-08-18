---
description: In der folgenden Tabelle sind alle HRESULT-Werte aufgeführt, die von den Methoden in der XPS Digital Signature-API zurückgegeben werden können.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: FEHLER bei der API für digitale XPS-Signaturen (Xpsdigitalsignature.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e40cea4b7d0e9997157c8b18c7f364ac7ac58b2b9edc6faec62cbe98685fcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711360"
---
# <a name="xps-digital-signature-api-errors"></a>Fehler bei der API für digitale XPS-Signaturen

In der folgenden Tabelle sind alle **HRESULT-Werte** aufgeführt, die von den Methoden in der XPS Digital Signature-API zurückgegeben werden können. Beachten Sie, dass nicht jede Methode jeden in dieser Tabelle aufgeführten Rückgabewert zurückgeben kann.



| Rückgabecode/-wert                                                                                                                                                                                                                                                                                  | Beschreibung                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>                                                                                                                                                                 | Die Methode wurde erfolgreich ausgeführt.<br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <dt>**XPS \_ E \_ UNGÜLTIGES \_ \_ SIGNATUREBLOCK-MARKUP**</dt> <dt>0x8052038b</dt> </dl> | Fehler im XML-Markup des Signaturblocks, während das Signaturmarkup gelesen wurde.<br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <dt>**XPS \_ E \_ MARKUP \_ COMPATIBILITY \_ ELEMENTS**</dt> <dt>0x80520389</dt> </dl> | Der [**XPS \_ SIGN \_ FLAGS-Wert**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) hat angegeben, dass keine Markupkompatibilitätselemente erwartet wurden. Markupkompatibilitätselemente wurden jedoch gefunden.<br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <dt>**XPS \_ \_E OBJECT \_ DETACHED**</dt> <dt>0x8052038a</dt> </dl>                                            | Die Schnittstelle ist dem Signatur-Manager nicht zugeordnet.<br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <dt>**XPS \_ E \_ PACKAGE \_ ALREADY \_ OPENED**</dt> <dt>0x80520387</dt> </dl>                      | Ein XPS-Paket wurde bereits im Signatur-Manager geöffnet. <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <dt>**XPS \_ E \_ PACKAGE \_ NOT \_ OPENED**</dt> <dt>0x80520386</dt> </dl>                                  | Ein XPS-Paket wurde noch nicht im Signatur-Manager geöffnet. <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <dt>**XPS \_ E \_ SIGNATUREID \_ DUP**</dt> <dt>0x80520388</dt> </dl>                                            | Zwei oder mehr Signaturen haben die gleiche ID.<br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <dt>**XPS \_ E \_ SIGREQUESTID \_ DUP**</dt> <dt>0x80520385</dt> </dl>                                         | Die Signaturanforderungs-ID ist innerhalb des Signaturblocks nicht eindeutig.<br/>                                                                                                     |



 

## <a name="remarks"></a>Hinweise

Einige METHODEN der DIGITALEN SIGNATUR-API von XPS rufen die [Paket-API](/previous-versions/windows/desktop/opc/packaging) auf. Informationen zu den Rückgabewerten der Paket-API finden Sie unter [Paketfehler.](/previous-versions/windows/desktop/opc/packaging-errors)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                            |
| Header<br/>                   | <dl> <dt>Xpsdigitalsignature.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>XpsDigitalSignature.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Fehlerbehandlung in COM](../com/error-handling-in-com.md)
</dt> <dt>

[Paketierungsfehler](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[Kryptografierückgabewerte](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

