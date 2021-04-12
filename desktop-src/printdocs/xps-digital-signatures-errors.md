---
description: In der folgenden Tabelle werden alle HRESULT-Werte aufgelistet, die von den Methoden in der XPS Digital Signature-API zurückgegeben werden können.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: XPS-Fehler bei der digitalen Signatur-API (XpsDigitalSignature. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82c6f5efe7e67d27f7d94b5d1db2732139fa59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348209"
---
# <a name="xps-digital-signature-api-errors"></a>XPS-Fehler bei der digitalen Signatur-API

In der folgenden Tabelle werden alle **HRESULT** -Werte aufgelistet, die von den Methoden in der XPS Digital Signature-API zurückgegeben werden können. Beachten Sie, dass nicht jede Methode jeden in dieser Tabelle aufgelisteten Rückgabewert zurückgeben kann.



| Rückgabecode/-wert                                                                                                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>                                                                                                                                                                 | Die Methode wurde erfolgreich ausgeführt.<br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <dt>**XPS \_ E \_ ungültiges \_ signatureblock- \_ Markup**</dt> <dt>0x8052038b</dt> </dl> | Fehler im XML-Markup des Signatur Blocks beim Lesen des Signatur Markups.<br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <dt>**XPS \_ E \_ Markup \_ Kompatibilitäts \_ Elemente**</dt> <dt>0x80520389</dt> </dl> | Der Wert für die [**XPS- \_ Signier \_ Flags**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) hat angegeben, dass keine Markup Kompatibilitäts Elemente erwartet wurden, aber es wurden Markup Kompatibilitäts Elemente gefunden.<br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <dt>**XPS \_ E- \_ Objekt \_ getrennt**</dt> <dt>0x8052038a</dt> </dl>                                            | Die Schnittstelle ist nicht dem Signatur-Manager zugeordnet.<br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <dt>**XPS \_ E- \_ Paket \_ bereits \_ geöffnet**</dt> <dt>0x80520387</dt> </dl>                      | Ein XPS-Paket wurde bereits im Signatur-Manager geöffnet. <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <dt>**XPS \_ E- \_ Paket \_ nicht \_ geöffnet**</dt> <dt>0x80520386</dt> </dl>                                  | Ein XPS-Paket wurde noch nicht im Signatur-Manager geöffnet. <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <dt>**XPS \_ E \_ signatureId \_ DUP**</dt> <dt>0x80520388</dt> </dl>                                            | Mindestens zwei Signaturen haben dieselbe ID.<br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <dt>**XPS \_ E \_ sigrequestid \_ DUP**</dt> <dt>0x80520385</dt> </dl>                                         | Die ID der Signatur Anforderung ist innerhalb des Signatur Blocks nicht eindeutig.<br/>                                                                                                     |



 

## <a name="remarks"></a>Bemerkungen

Einige Methoden der digitalen XPS-Signatur-API führen Aufrufe an die [Paketierungs](/previous-versions/windows/desktop/opc/packaging) -API aus. Informationen zu den Rückgabe Werten der Packungs-API finden Sie unter [Packen von Fehlern](/previous-versions/windows/desktop/opc/packaging-errors).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                            |
| Header<br/>                   | <dl> <dt>XpsDigitalSignature. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>XpsDigitalSignature. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehlerbehandlung in com](../com/error-handling-in-com.md)
</dt> <dt>

[Paketfehler](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[Kryptografierückgabetwerte](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

