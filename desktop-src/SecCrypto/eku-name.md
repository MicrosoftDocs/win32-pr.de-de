---
description: Legt einen Enumerationswert fest, der den CAPICOM-Namen der EKU angibt, oder ruft ihn ab. Dies ist die Standard Eigenschaft.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: 'Ieku:: Name-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373908"
---
# <a name="iekuname-property"></a>Ieku:: Name-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **Name** -Eigenschaft legt einen Enumerationswert fest, der den CAPICOM-Namen der EKU angibt, oder ruft ihn ab. Dies ist die Standard Eigenschaft.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM \_ EKU**](capicom-eku.md) -Enumeration, der den CAPICOM-Namen der EKU angibt. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <dt>**Weitere CAPICOM- \_ EKU \_ other**</dt> </dl>                                                      | Das Zertifikat verfügt über in der lokalen Richtlinie definierte Verwendung. Diese wird verwendet, wenn die erforderliche EKU nicht vordefiniert ist und der OID-Wert von der Anwendung festgelegt werden muss.<br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <dt>**CAPICOM- \_ EKU- \_ Server Authentifizierung \_**</dt> </dl>                                   | Das Zertifikat kann zum Authentifizieren eines Servers verwendet werden.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <dt>**CAPICOM- \_ EKU- \_ Client Authentifizierung \_**</dt> </dl>                                   | Das Zertifikat kann zum Authentifizieren eines Clients verwendet werden.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <dt>**CAPICOM- \_ EKU- \_ Code \_ Signatur**</dt> </dl>                                | Das Zertifikat kann verwendet werden, um eine digitale Signatur zu erstellen.<br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <dt>**CAPICOM \_ EKU \_ -e-Mail- \_ Schutz**</dt> </dl>                    | Zertifikat kann für den e-Mail-Schutz verwendet werden.<br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <dt>**CAPICOM \_ EKU \_ Smartcard- \_ Anmeldung**</dt> </dl>                       | Das Zertifikat kann für die Smartcard-Anmeldung verwendet werden. Eingeführt in CAPICOM 2,0.<br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <dt>**CAPICOM- \_ EKU- \_ verschlüsselndes \_ Datei \_ System**</dt> </dl> | Das Zertifikat kann für EFS verwendet werden. Eingeführt in CAPICOM 2,0.<br/>                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
