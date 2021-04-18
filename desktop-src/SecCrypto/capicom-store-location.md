---
description: Gibt den Speicherort eines Zertifikat Speicher an.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: CAPICOM_STORE_LOCATION-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 24b2e786e2821c39c6ff67f5919dca2ac0c6bfe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358684"
---
# <a name="capicom_store_location-enumeration"></a>CAPICOM \_ Store \_ Location-Enumeration

Der Enumerationstyp " **CAPICOM \_ Store \_ Location** " gibt den Speicherort eines [*Zertifikat Speicher*](../secgloss/c-gly.md)an.

## <a name="members"></a>Member



| Member                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                      | Wert |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM- \_ Speicher Speicher \_**                  | Der Speicher ist ein Speicher Speicher. Alle Änderungen im Inhalt des Stores werden nicht persistent gespeichert.<br/>                                                                                                                                                                              | 0     |
| **lokaler CAPICOM- \_ \_ Computer \_ Speicher**          | Der Speicher ist ein lokaler Computerspeicher. Lokale Computerspeicher können nur Lese-/Schreibspeicher sein, wenn der Benutzer über Lese-/Schreibberechtigungen verfügt. Wenn der Benutzer über Lese-/Schreibberechtigungen verfügt und der Speicher mit Lese-/Schreibzugriff geöffnet wird, werden Änderungen im Inhalt des Stores beibehalten.<br/> | 1     |
| **CAPICOM \_ aktueller \_ Benutzer \_ Speicher**           | Der Speicher ist ein aktueller Benutzerspeicher. Ein aktueller Benutzerspeicher kann ein Lese-/Schreibspeicher sein. Wenn dies der Fall ist, werden Änderungen am Inhalt des Stores persistent gespeichert.<br/>                                                                                                                      | 2     |
| **CAPICOM \_ Active \_ Directory- \_ Benutzer \_ Speicher** | Der Speicher ist ein Active Directory Speicher. Active Directory Stores können nur im schreibgeschützten Modus geöffnet werden. Zertifikate können Active Directory speichern nicht hinzugefügt oder daraus entfernt werden.<br/>                                                                                        | 3     |
| **CAPICOM \_ - \_ Smartcard- \_ Benutzer \_ Speicher**       | Stores unterstützen Smartcard – basierte Zertifikat Speicher. Der Speicher ist die Gruppe der vorhandenen Smartcards. Eingeführt in CAPICOM 2,0.<br/>                                                                                                                                         | 4     |



## <a name="remarks"></a>Bemerkungen

Der Enumerationstyp " **CAPICOM \_ Store \_ Location** " wird von den folgenden Methoden verwendet:

-   [**PrivateKey. Open**](privatekey-open.md)
-   [**Store. Open**](store-open.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
