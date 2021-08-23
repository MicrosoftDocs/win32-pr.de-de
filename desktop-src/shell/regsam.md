---
description: Ein Datentyp, der zum Angeben der Sicherheitszugriffsattribute in der Registrierung verwendet wird.
title: REGSAM (Winnt.h)
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
ms.openlocfilehash: e202e615561ce0c51f44fc39726d8ab864afc2b5e1bcbbe5612edbb74c476c29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820420"
---
# <a name="regsam"></a>REGSAM

Ein Datentyp, der zum Angeben der Sicherheitszugriffsattribute in der Registrierung verwendet wird.



| Konstante                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <dt>**KEY \_ ALL \_ ACCESS**</dt> </dl>                          | Kombination der Zugriffe "KEY \_ QUERY \_ VALUE", "KEY \_ ENUMERATE \_ SUB \_ KEYS", "KEY \_ NOTIFY", "KEY \_ CREATE SUB \_ \_ KEY", "KEY \_ CREATE \_ LINK" und "KEY \_ SET \_ VALUE".<br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <dt>**KEY \_ CREATE \_ LINK**</dt> </dl>                       | Berechtigung zum Erstellen einer symbolischen Verknüpfung.<br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <dt>**KEY \_ CREATE \_ SUB \_ KEY**</dt> </dl>             | Berechtigung zum Erstellen von Unterschlüsseln.<br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <dt>**SCHLÜSSEL \_ AUFZÄHLEN VON \_ \_ UNTERSCHLÜSSELN**</dt> </dl> | Berechtigung zum Aufzählen von Unterschlüsseln.<br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <dt>**KEY \_ EXECUTE**</dt> </dl>                                    | Berechtigung für Lesezugriff.<br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <dt>**\_SCHLÜSSELBENACHRICHTIGUNG**</dt> </dl>                                       | Berechtigung für Änderungsbenachrichtigungen.<br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <dt>**\_ \_ SCHLÜSSELABFRAGEWERT**</dt> </dl>                       | Berechtigung zum Abfragen von Unterschlüsseldaten.<br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <dt>**KEY \_ READ**</dt> </dl>                                             | Kombination aus dem Zugriff "KEY \_ QUERY \_ VALUE", "KEY \_ ENUMERATE \_ SUB \_ KEYS", und "KEY \_ NOTIFY".<br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <dt>**KEY \_ SET \_ VALUE**</dt> </dl>                             | Berechtigung zum Festlegen von Unterschlüsseldaten.<br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <dt>**KEY \_ WRITE**</dt> </dl>                                          | Kombination aus dem Zugriff "KEY \_ SET \_ VALUE" und "KEY \_ CREATE SUB \_ \_ KEY".<br/>                                                                                                                |



## <a name="remarks"></a>Hinweise

Ein **REGSAM-Wert** kann einer oder mehrere der aufgelisteten Werte sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winnt.h</dt> </dl> |



 

 




