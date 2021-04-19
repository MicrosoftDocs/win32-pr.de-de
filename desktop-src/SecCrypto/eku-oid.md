---
description: Legt eine Zeichenfolge fest oder ruft eine Zeichenfolge ab, die einen EKU-OID-Zeichen folgen Wert enthält, wie in Wincrypt. h
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: 'Ieku:: OID (Eigenschaft)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 77a519051d2bd1cb3c948bf0e2271cced7d80a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370222"
---
# <a name="iekuoid-property"></a>Ieku:: OID (Eigenschaft)

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **OID** -Eigenschaft legt eine Zeichenfolge fest oder ruft Sie ab, die einen EKU-OID-Zeichen folgen Wert enthält, wie in Wincrypt. h definiert.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
EKU.OID As String
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die den EKU-OID-Zeichen folgen Wert enthält, wie in Wincrypt. h definiert.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft verwendet nicht das in CAPICOM 2,0 eingeführte [**OID**](oid.md) -Objekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
