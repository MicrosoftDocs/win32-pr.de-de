---
description: Legt die Zertifikatoption des Signierers fest oder ruft sie ab.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Signer.Options-Eigenschaft
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
ms.openlocfilehash: 7b4a787524e967b5356ed7fb5531a3ec7d7dbfb99d57fc75217a82f220468db7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898836"
---
# <a name="signeroptions-property"></a>Signer.Options-Eigenschaft

\[Die **Options-Eigenschaft** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Options-Eigenschaft** legt die Zertifikatoption des Signierers fest oder ruft sie ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM \_ CERTIFICATE INCLUDE \_ \_ OPTION-Enumeration,**](capicom-certificate-include-option.md) der die Zertifikatoption des Signierers angibt. Der Standardwert ist CAPICOM \_ CERTIFICATE INCLUDE CHAIN EXCEPT \_ \_ \_ \_ ROOT. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                                                                             | Bedeutung                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ INCLUDE \_ CHAIN \_ EXCEPT \_ ROOT**</dt> </dl> | Speichert alle Zertifikate in der Kette mit Ausnahme der Stammentität.<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**\_CAPICOM-ZERTIFIKAT \_ UMFASST GANZE \_ \_ KETTE**</dt> </dl>                    | Speichert die vollständige Zertifikatkette.<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**CAPICOM \_ CERTIFICATE INCLUDE END ENTITY ONLY (CAPICOM-ZERTIFIKAT \_ \_ \_ NUR ENDENTITÄT EINSCHLIEßEN) \_**</dt> </dl>       | Speichert nur das Endentitätszertifikat.<br/>                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Signer**](signer.md)
</dt> </dl>

 

 
