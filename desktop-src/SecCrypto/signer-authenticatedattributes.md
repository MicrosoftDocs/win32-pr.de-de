---
description: Ruft die Auflistung der authentifizierten Attribute ab.
ms.assetid: d4b3efab-d71e-4fef-9691-0c0bbcb27281
title: Signer. authenticatedattributes-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.AuthenticatedAttributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3963ec60d699300c4cde368d4d78c39c0873edd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354042"
---
# <a name="signerauthenticatedattributes-property"></a>Signer. authenticatedattributes-Eigenschaft

\[Die **authenticatedattributes** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **authenticatedattributes** -Eigenschaft ruft die Auflistung der authentifizierten Attribute ab.

## <a name="syntax"></a>Syntax


```VB
Signer.AuthenticatedAttributes As Attributes
```



## <a name="property-value"></a>Eigenschaftswert

Eine [**Attribut**](attributes.md) Auflistung, die die authentifizierten Attribute des Signatur Gebers darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signatur Geber**](signer.md)
</dt> </dl>

 

 
