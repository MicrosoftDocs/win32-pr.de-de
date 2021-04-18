---
description: Legt die Zertifikat Option des Signatur Gebers fest oder ruft Sie ab.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Signer. Options (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c22cf7b9d9ebe7e98e534d62b0a2771391c6cacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365683"
---
# <a name="signeroptions-property"></a>Signer. Options (Eigenschaft)

\[Die **options** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **options** -Eigenschaft legt die Zertifikat Option des Signatur Gebers fest oder ruft Sie ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM \_ Certificate \_ include- \_ Option**](capicom-certificate-include-option.md) -Enumeration, die die Zertifikat Option des Signatur Gebers angibt. Der Standardwert ist CAPICOM \_ Certificate \_ include \_ Chain, \_ ausgenommen \_ root. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                                             | Bedeutung                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**CAPICOM- \_ Zertifikats \_ include- \_ Kette \_ mit Ausnahme von \_ root**</dt> </dl> | Speichert alle Zertifikate in der Kette mit Ausnahme der Stamm Entität.<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**CAPICOM- \_ Zertifikat \_ einschließlich \_ ganzer \_ Kette**</dt> </dl>                    | Speichert die komplette Zertifikatskette.<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**CAPICOM- \_ Zertifikat \_ schließt \_ nur End- \_ Entität \_ ein.**</dt> </dl>       | Speichert nur das Endentitäts Zertifikat.<br/>                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signatur Geber**](signer.md)
</dt> </dl>

 

 
