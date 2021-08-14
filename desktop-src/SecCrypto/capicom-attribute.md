---
description: Definiert die Art des Attributs, das einer Signatur zugeordnet ist.
ms.assetid: 94f0dce4-0b32-4c39-ab2e-b01795432acd
title: CAPICOM_ATTRIBUTE -Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ATTRIBUTE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 26562af3716648540843684bf6c7c901174d36ee1bd615a75d3d98094cc61c77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772816"
---
# <a name="capicom_attribute-enumeration"></a>CAPICOM \_ ATTRIBUTE-Enumeration

Der **CAPICOM \_ ATTRIBUTE-Enumerationstyp** definiert die Art des Attributs, das einer Signatur [*zugeordnet ist.*](../secgloss/d-gly.md)

## <a name="members"></a>Member



| Member                                                       | BESCHREIBUNG                                                                | Wert |
|--------------------------------------------------------------|----------------------------------------------------------------------------|-------|
| **SIGNIERUNGSZEIT FÜR \_ CAPICOM-AUTHENTIFIZIERTE \_ \_ \_ ATTRIBUTE**         | Das -Attribut enthält den Zeitpunkt, zu dem die Signatur erstellt wurde.<br/> | 0     |
| **DOKUMENTNAME DES \_ AUTHENTIFIZIERTEN CAPICOM-ATTRIBUTS \_ \_ \_**        | Das Attribut enthält den Namen des signierten Dokuments.<br/>         | 1     |
| **DOKUMENTBESCHREIBUNG DES AUTHENTIFIZIERTEN \_ \_ CAPICOM-ATTRIBUTS \_ \_** | Das -Attribut enthält eine Beschreibung des signierten Dokuments.<br/>    | 2     |



## <a name="remarks"></a>Hinweise

Der **CAPICOM \_ ATTRIBUTE-Enumerationstyp** wird von der [**Attribute.Name**](attribute-name.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
