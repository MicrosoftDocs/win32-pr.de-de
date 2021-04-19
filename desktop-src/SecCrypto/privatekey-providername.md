---
description: Ruft den Namen des Kryptografiedienstanbieters (CSP) ab.
ms.assetid: b06d2839-0eaa-4f3f-99f7-d77e001fe4ea
title: PrivateKey. ProviderName-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 528117db072b80ab6d9203b8b2fc2786175499ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365802"
---
# <a name="privatekeyprovidername-property"></a>PrivateKey. ProviderName-Eigenschaft

\[Die **providerName** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Certificate2. PrivateKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **providerName** -Eigenschaft ruft den Namen des [*Kryptografiedienstanbieters (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) ab.

## <a name="syntax"></a>Syntax


```VB
PrivateKey.ProviderName As String
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die den Namen des CSP enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
