---
description: Gibt den Speicherort eines Zertifikatspeichers an.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: CAPICOM_STORE_LOCATION -Enumeration (Capicom.h)
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
ms.openlocfilehash: 15aa93b70840e13901f88c40c715024ec33a835be14b7453da99aecae079b487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879010"
---
# <a name="capicom_store_location-enumeration"></a>CAPICOM \_ STORE \_ LOCATION-Enumeration

Der **CAPICOM \_ STORE \_ LOCATION-Enumerationstyp** gibt den Speicherort eines [*Zertifikatspeichers an.*](../secgloss/c-gly.md)

## <a name="members"></a>Member



| Member                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                      | Wert |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_CAPICOM-SPEICHER \_**                  | Der Speicher ist ein Speicher. Änderungen am Inhalt des Speichers werden nicht beibehalten.<br/>                                                                                                                                                                              | 0     |
| **\_CAPICOM-SPEICHER \_ FÜR LOKALE \_ COMPUTER**          | Der Speicher ist ein lokaler Computerspeicher. Lokale Computerspeicher können nur dann Lese-/Schreibspeicher sein, wenn der Benutzer über Lese-/Schreibberechtigungen verfügt. Wenn der Benutzer über Lese-/Schreibberechtigungen verfügt und der Speicher mit Lese-/Schreibzugriff geöffnet wird, werden Änderungen am Inhalt des Speichers beibehalten.<br/> | 1     |
| **CAPICOM \_ CURRENT \_ USER \_ STORE**           | Der Speicher ist ein aktueller Benutzerspeicher. Ein aktueller Benutzerspeicher kann ein Lese-/Schreibspeicher sein. Wenn dies der Wert ist, werden Änderungen am Inhalt des Speichers beibehalten.<br/>                                                                                                                      | 2     |
| **CAPICOM \_ ACTIVE \_ \_ DIRECTORY-BENUTZERSPEICHER \_** | Der Speicher ist ein Active Directory-Speicher. Active Directory-Speicher können nur im schreibgeschützten Modus geöffnet werden. Zertifikate können active Directory-Speichern nicht hinzugefügt oder daraus entfernt werden.<br/>                                                                                        | 3     |
| **CAPICOM \_ \_ \_ SMARTCARD-BENUTZERSPEICHER \_**       | Speicher unterstützen Smartcard-basierte Zertifikatspeicher. Der Store ist die Gruppe der aktuellen Smartcards. Eingeführt in CAPICOM 2.0.<br/>                                                                                                                                         | 4     |



## <a name="remarks"></a>Hinweise

Der **CAPICOM \_ STORE \_ LOCATION-Enumerationstyp** wird von den folgenden Methoden verwendet:

-   [**PrivateKey.Open**](privatekey-open.md)
-   [**Store. Öffnen**](store-open.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
