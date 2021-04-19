---
description: Ruft die Objekt-ID des Qualifizierers ab.
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: Qualifizierer. Oid-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a86aaf7b60b98811e2d1fbef79c520448f1d47f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370743"
---
# <a name="qualifieroid-property"></a>Qualifizierer. Oid-Eigenschaft

\[Die **OID** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung sind.\]

Die **OID** -Eigenschaft ruft die Objekt-ID des Qualifizierers ab. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**OID**](oid.md) -Objekt, das den Qualifizierer identifiziert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Qualifizierer**](qualifier.md)
</dt> </dl>

 

 
