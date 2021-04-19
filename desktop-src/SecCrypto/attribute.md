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
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370818"
---
# <a name="attribute-object"></a>Attribute-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**cryptographiertributeobject-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/previous-versions/windows/) -Namespace.\]

Das **Attribut** Objekt stellt ein einzelnes authentifiziertes Attribut dar.

## <a name="when-to-use"></a>Verwendung

Das **Attribut** Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Festlegen oder Abrufen des CAPICOM-namens des Attributs.
-   Legen Sie den Wert des Attributs fest, oder rufen Sie ihn ab, wie z. b. die Signatur Zeit, den Namen des signierten Dokuments oder eine Beschreibung des signierten Dokuments.

## <a name="members"></a>Member

Das **Attribut** Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Attribut** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                    | Zugriffstyp           | BESCHREIBUNG                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**Name**](attribute-name.md)<br/>   | Lesen/Schreiben<br/> | Legt den CAPICOM-Namen des Attributs fest oder ruft ihn ab. Dies ist die Standard Eigenschaft.<br/> |
| [**Wert**](attribute-value.md)<br/> | Lesen/Schreiben<br/> | Legt den Wert des Attributs fest oder ruft ihn ab.<br/>                                      |



 

## <a name="remarks"></a>Bemerkungen

Das **Attribut** Objekt kann erstellt werden und ist für die Skripterstellung sicher. Die ProgID für das **Attribut** Objekt ist "CAPICOM". Attribut. 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
