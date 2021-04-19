---
description: Legt den Wert des Attributs fest oder ruft ihn ab.
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Attribute. Value-Eigenschaft
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
ms.openlocfilehash: 6b3d2f41c56fc47277bd71354279e75b423d0c0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361611"
---
# <a name="attributevalue-property"></a>Attribute. Value-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**cryptographiertributeobject-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/previous-versions/windows/) -Namespace.\]

Die **value** -Eigenschaft legt den Wert des Attributs fest oder ruft ihn ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a>Eigenschaftswert

Eine **Variant** -Variable, die den Wert des Attributs enthält. Für **\_ authentifizierte CAPICOM \_ Attribute \_ SIGNING \_ time** -Attribute ist der Datentyp **Date**. Für alle anderen Attribute ist der Eigenschafts Wert eine Zeichenfolge.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
