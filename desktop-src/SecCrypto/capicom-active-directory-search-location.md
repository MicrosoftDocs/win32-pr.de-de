---
description: Gibt den Speicherort an, der nach einem Active Directory Zertifikat Speicher gesucht werden soll.
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: cd630bdc0c09a6bb57a9163ec972451011f3e826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351237"
---
# <a name="capicom_active_directory_search_location-enumeration"></a>CAPICOM- \_ Active \_ Directory- \_ \_ Suchspeicherort-Enumeration

Der Enumerationstyp " **CAPICOM \_ Active \_ Directory- \_ \_ Suchort** " gibt den Speicherort an, der nach einem Active Directory [*Zertifikat Speicher*](../secgloss/c-gly.md)gesucht werden soll.

## <a name="members"></a>Member



| Member                               | BESCHREIBUNG                                  | Wert |
|--------------------------------------|----------------------------------------------|-------|
| **CAPICOM- \_ Suche \_ Any**             | Durchsucht alle verfügbaren Speicherorte.<br/> | 0     |
| **CAPICOM- \_ Suche ( \_ globaler \_ Katalog)** | Durchsucht nur den globalen Katalog.<br/> | 1     |
| **\_ \_ Standard \_ Domäne für CAPICOM-Suche** | Durchsucht nur die Standard Domäne.<br/> | 2     |



## <a name="remarks"></a>Bemerkungen

Dieser Enumerationstyp wird von der folgenden Eigenschaft verwendet:

-   [**Settings. activedirectoriysearchlocation**](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
