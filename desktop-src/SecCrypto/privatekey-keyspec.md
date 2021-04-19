---
description: Ruft die Schlüssel Spezifikation ab.
ms.assetid: 93c909cb-b1d1-4c2b-a66c-9d3f6dd9b340
title: PrivateKey. KeySpec-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.KeySpec
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f9d0ba55ca48d5257a038845f84374544b7615b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361377"
---
# <a name="privatekeykeyspec-property"></a>PrivateKey. KeySpec-Eigenschaft

\[Die **KeySpec** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Certificate2. PrivateKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **KeySpec** -Eigenschaft ruft die Schlüssel Spezifikation ab.

## <a name="syntax"></a>Syntax


```VB
PrivateKey.KeySpec As CAPICOM_KEY_SPEC
```



## <a name="property-value"></a>Eigenschaftswert

Ein Wert der [**CAPICOM- \_ schlüsselspezifikations \_**](capicom-key-spec.md) Enumeration, der die Schlüssel Spezifikation angibt. In der folgenden Tabelle sind die möglichen Werte aufgeführt.



| Wert                                                                                                                                                                                                        | Bedeutung                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <dt>**CAPICOM- \_ Schlüssel \_ Spezifikation \_ keyexchange**</dt> </dl> | Der Schlüssel kann für die Verschlüsselung und Signierung verwendet werden.<br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <dt>**CAPICOM \_ Key \_ spec- \_ Signatur**</dt> </dl>       | Der Schlüssel kann nur für die Signierung verwendet werden.<br/>           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
