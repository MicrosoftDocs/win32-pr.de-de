---
description: Stellt ein einzelnes authentifiziertes Attribut dar.
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Attribute-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c3e07c771a34e89cfbcbba5695450e195ef55482e0a27bee008f3ea8251bf8bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879870"
---
# <a name="attribute-object"></a>Attribute-Objekt

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**CryptographicAttributeObject-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography-Namespace.**](/previous-versions/windows/)\]

Das **Attributobjekt** stellt ein einzelnes authentifiziertes Attribut dar.

## <a name="when-to-use"></a>Verwendung

Das **Attributobjekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Legen Sie den CAPICOM-Namen des Attributs fest, oder rufen Sie den Namen ab.
-   Legen Sie den Wert des Attributs fest, z. B. die Signierungszeit, den Namen des signierten Dokuments oder eine Beschreibung des signierten Dokuments, oder rufen Sie diesen wert ab.

## <a name="members"></a>Member

Das **Attribute-Objekt** weist diese Typen von Membern auf:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Attributobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                    | Zugriffstyp           | BESCHREIBUNG                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**Name**](attribute-name.md)<br/>   | Lesen/Schreiben<br/> | Legt den CAPICOM-Namen des Attributs fest oder ruft sie ab. Dies ist die Standardeigenschaft.<br/> |
| [**Wert**](attribute-value.md)<br/> | Lesen/Schreiben<br/> | Legt den Wert des Attributs fest oder ruft den Wert ab.<br/>                                      |



 

## <a name="remarks"></a>Hinweise

Das **Attributobjekt** kann erstellt werden und ist für Skripts sicher. Die ProgID für das **Attributobjekt** ist CAPICOM. Attribute.1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
