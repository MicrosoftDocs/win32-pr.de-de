---
description: Ruft den Inhalt des Benutzerhinweises ab.
ms.assetid: dcf73357-253d-4160-be4e-f826296f5eaa
title: Qualifier.ExplicitText-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.ExplicitText
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 60753e0e7fa9996f9584070d6fac2d12d3a483b681fa61b72cf2e59cc2898995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901111"
---
# <a name="qualifierexplicittext-property"></a>Qualifier.ExplicitText-Eigenschaft

\[Die **ExplicitText-Eigenschaft** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates,**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikatrichtlinien verwenden, um Qualifizierer zu verarbeiten, die Teil der Richtlinieninformationen in der Zertifikatrichtlinienerweiterung sind.\]

Die **ExplicitText-Eigenschaft** ruft den Inhalt des Benutzerhinweises ab. Diese Eigenschaft ist möglicherweise leer.

## <a name="syntax"></a>Syntax


```VB
Qualifier.ExplicitText As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Inhalt des Benutzerhinweises.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Qualifizierer**](qualifier.md)
</dt> </dl>

 

 
