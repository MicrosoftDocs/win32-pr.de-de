---
description: Legt einen Enumerationswert fest, der den CAPICOM-Namen der EKU angibt, oder ruft diesen ab. Dies ist die Standardeigenschaft.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: IEKU::Name-Eigenschaft
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
ms.openlocfilehash: ca1564b943874ec086dd5e4459e69543cbdc90ebde2a11a2084c3054e3727dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767228"
---
# <a name="iekuname-property"></a>IEKU::Name-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System.Security.Cryptography.X509Certificates-Namespace.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Name-Eigenschaft** legt einen Enumerationswert fest oder ruft diesen ab, der den CAPICOM-Namen der EKU angibt. Dies ist die Standardeigenschaft.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM-EKU-Enumeration, \_**](capicom-eku.md) der den CAPICOM-Namen der EKU angibt. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <dt>**CAPICOM \_ EKU \_ OTHER**</dt> </dl>                                                      | Für das Zertifikat wurden in der lokalen Richtlinie definierte Verwendungen verwendet. Dies wird verwendet, wenn die benötigte EKU nicht vordefiniert ist und der OID-Wert von der Anwendung festgelegt werden muss.<br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <dt>**CAPICOM \_ EKU \_ SERVER \_ AUTH**</dt> </dl>                                   | Das Zertifikat kann zum Authentifizieren eines Servers verwendet werden.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <dt>**CAPICOM \_ EKU \_ CLIENT \_ AUTH**</dt> </dl>                                   | Das Zertifikat kann zum Authentifizieren eines Clients verwendet werden.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <dt>**\_ \_ CAPICOM-EKU-CODESIGNATUR \_**</dt> </dl>                                | Zertifikat kann zum Erstellen einer digitalen Signatur verwendet werden.<br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <dt>**CAPICOM \_ EKU \_ EMAIL \_ PROTECTION**</dt> </dl>                    | Das Zertifikat kann für den E-Mail-Schutz verwendet werden.<br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <dt>**CAPICOM \_ EKU \_ \_ SMARTCARD-ANMELDUNG**</dt> </dl>                       | Das Zertifikat kann für die Smartcardanmeldung verwendet werden. Eingeführt in CAPICOM 2.0.<br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <dt>**CAPICOM \_ EKU \_ ENCRYPTING \_ FILE \_ SYSTEM**</dt> </dl> | Das Zertifikat kann für EFS verwendet werden. Eingeführt in CAPICOM 2.0.<br/>                                                                                      |



 

## <a name="remarks"></a>Hinweise

Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Zustand*](../secgloss/s-gly.md) des Objekts zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
