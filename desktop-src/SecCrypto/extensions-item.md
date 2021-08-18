---
description: Die Item-Eigenschaft ruft eine Erweiterung nach Index aus der Auflistung ab. Dies ist die Standardeigenschaft.
ms.assetid: 0242dc14-abf2-49df-b75a-9005b2376cfc
title: Extensions.Item-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8e340aff8fb952e665bbfaae31f58a086459ccf2821954221ba9d730766638c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006848"
---
# <a name="extensionsitem-property"></a>Extensions.Item-Eigenschaft

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ExtensionCollection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Item-Eigenschaft** ruft eine Erweiterung nach Index aus der Auflistung ab. Dies ist die Standardeigenschaft.

## <a name="syntax"></a>Syntax


```VB
Extensions.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**Extension-Objekt,**](extension.md) das die indizierte Zertifikaterweiterung der Auflistung darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Erweiterungen**](extensions.md)
</dt> </dl>

 

 
