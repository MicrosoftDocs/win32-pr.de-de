---
description: Ruft den Namen der Vorlage ab.
ms.assetid: f92346bc-89b6-4063-aa66-85e2fb88d67d
title: Template.Name-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8c6d9207712d5154dbe74b61a288f3f4591cacb1f277ad04408648472dac23af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972111"
---
# <a name="templatename-property"></a>Template.Name-Eigenschaft

\[Die **Name-Eigenschaft** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates,**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) indem Sie den Konstruktor aufrufen, der eine OID als Parameter akzeptiert, und dann die OID für Zertifikatvorlage verwenden, um die Zertifikaterweiterungsvorlage abzurufen.\]

Die **Name-Eigenschaft** ruft den Namen der Vorlage ab.

## <a name="syntax"></a>Syntax


```VB
Template.Name As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Name der Vorlage.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Vorlage**](template.md)
</dt> </dl>

 

 
