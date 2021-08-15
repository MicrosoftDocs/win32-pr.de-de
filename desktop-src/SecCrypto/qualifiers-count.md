---
description: Ruft die Anzahl der Qualifiziererobjekte in der Auflistung ab.
ms.assetid: 9dafb83a-ff7f-4317-8ed4-2a46dcebf409
title: Qualifiers.Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fd4cfe0d600c99251db77b1764edb83353b01143fc5179c1efc29673e30e734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900946"
---
# <a name="qualifierscount-property"></a>Qualifiers.Count-Eigenschaft

\[Die **Count-Eigenschaft** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates,**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) indem Sie den Konstruktor aufrufen, der eine OID als Parameter akzeptiert, und dann die OID für Zertifikatrichtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinieninformationen in der Zertifikatrichtlinienerweiterung sind.\]

Die **Count-Eigenschaft** ruft die Anzahl der [**Qualifiziererobjekte**](qualifier.md) in der Auflistung ab.

## <a name="syntax"></a>Syntax


```VB
Qualifiers.Count As Long
```



## <a name="property-value"></a>Eigenschaftswert

Anzahl der [**Qualifiziererobjekte**](qualifier.md) in der Auflistung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Qualifikation**](qualifiers.md)
</dt> </dl>

 

 
