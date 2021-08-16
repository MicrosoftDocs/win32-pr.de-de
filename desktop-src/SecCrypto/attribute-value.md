---
description: Legt den Wert des Attributs fest oder ruft den Wert ab.
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Attribute.Value-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41737e086f1889531322115c8ff57e64c8893063f498b2566f0010f0f3f0ca30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773704"
---
# <a name="attributevalue-property"></a>Attribute.Value-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**CryptographicAttributeObject-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography-Namespace.**](/previous-versions/windows/)\]

Die **Value-Eigenschaft** legt den Wert des Attributs fest oder ruft den Wert ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a>Eigenschaftswert

Eine **Variant-Variable,** die den Wert des Attributs enthält. Für **CAPICOM \_ AUTHENTICATED \_ ATTRIBUTE SIGNING \_ \_ TIME-Attribute** ist der Datentyp **DATE**. Für alle anderen Attribute ist der Eigenschaftswert eine Zeichenfolge.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
