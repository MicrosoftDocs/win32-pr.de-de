---
description: Ruft ein OID-Objekt ab, das das Template-Objekt identifiziert.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Template.OID-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecfc56210d5fa81f6e7623b2c471cf0df1b5f091f7dab6c797b56f6af8d2496e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897385"
---
# <a name="templateoid-property"></a>Template.OID-Eigenschaft

\[Die **OID-Eigenschaft** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates,**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) indem Sie den Konstruktor aufrufen, der eine OID als Parameter akzeptiert, und dann die OID für Zertifikatvorlage verwenden, um die Zertifikaterweiterungsvorlage abzurufen.\]

Die **OID-Eigenschaft** ruft ein [**OID-Objekt**](oid.md) ab, das das [**Template-Objekt identifiziert.**](template.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Template.OID As OID
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**OID-Objekt,**](oid.md) das das [**Template-Objekt**](template.md) identifiziert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Vorlage**](template.md)
</dt> </dl>

 

 
