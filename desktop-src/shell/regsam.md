---
description: Ein Datentyp, der zum Angeben der Sicherheits Zugriffs Attribute in der Registrierung verwendet wird.
title: Regsam (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2700e278f86db046d532b91b64bf5a2d00582e14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983085"
---
# <a name="regsam"></a>Regsam

Ein Datentyp, der zum Angeben der Sicherheits Zugriffs Attribute in der Registrierung verwendet wird.



| Konstante                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <dt>**Schlüssel \_ \_ Zugriff**</dt> </dl>                          | Kombination * * * * Key \_ Query \_ value * * * *, * * * * Key \_ Enumerate \_ Sub \_ Keys * * * *, * * * * Key \_ Notify * * * *, * * * * Key \_ Create \_ Sub \_ Key * * * *, * * * * Key \_ Create \_ Link * * * * und * * * * Key \_ Set \_ value * * * * Access.<br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <dt>**\_Link zum Erstellen von Schlüsseln \_**</dt> </dl>                       | Berechtigung zum Erstellen eines symbolischen Links.<br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <dt>**Key \_ Create \_ Sub \_ Key**</dt> </dl>             | Berechtigung zum Erstellen von unter Schlüsseln.<br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <dt>**Schlüssel \_ \_ Unterschlüssel aufzählen \_**</dt> </dl> | Berechtigung zum Aufzählen von unter Schlüsseln.<br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <dt>**Schlüssel \_ Ausführung**</dt> </dl>                                    | Berechtigung für Lesezugriff.<br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <dt>**Schlüssel \_ Benachrichtigung**</dt> </dl>                                       | Berechtigung für Änderungs Benachrichtigung.<br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <dt>**Schlüssel \_ Abfrage \_ Wert**</dt> </dl>                       | Berechtigung zum Abfragen von Unterschlüssel Daten.<br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <dt>**Schlüssel \_ Lesevorgang**</dt> </dl>                                             | Kombination aus * * * * Key \_ Query \_ value * * * *, * * * * Key \_ Enumerate \_ Sub \_ Keys * * * * und * * * * Key \_ Notify * * * * Access.<br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <dt>**Schlüssel \_ Satz \_ Wert**</dt> </dl>                             | Berechtigung zum Festlegen von Unterschlüssel Daten.<br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <dt>**Schlüssel \_ Schreibvorgang**</dt> </dl>                                          | Kombination aus * * * * Key \_ Set \_ Value * * * * und * * * * Key \_ Create \_ Sub \_ Key * * * * Access.<br/>                                                                                                                |



## <a name="remarks"></a>Bemerkungen

Bei einem **regsam** -Wert kann es sich um einen oder mehrere der aufgelisteten Werte handeln.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WinNT. h</dt> </dl> |



 

 




