---
title: Cache Gruppen Konstanten (WinInet. h)
description: Die folgende Liste enthält die Konstanten, die von den Cache Gruppenfunktionen verwendet werden.
ms.assetid: 9ca2069e-497d-4747-acf4-d5b8020b8ab7
topic_type:
- apiref
api_name:
- CACHEGROUP_ATTRIBUTE_BASIC
- CACHEGROUP_ATTRIBUTE_FLAG
- CACHEGROUP_ATTRIBUTE_GET_ALL
- CACHEGROUP_ATTRIBUTE_GROUPNAME
- CACHEGROUP_ATTRIBUTE_QUOTA
- CACHEGROUP_ATTRIBUTE_STORAGE
- CACHEGROUP_ATTRIBUTE_TYPE
- CACHEGROUP_FLAG_FLUSHURL_ONDELETE
- CACHEGROUP_FLAG_GIDONLY
- CACHEGROUP_FLAG_NONPURGEABLE
- CACHEGROUP_READWRITE_MASK
- CACHEGROUP_SEARCH_ALL
- CACHEGROUP_SEARCH_BYURL
- CACHEGROUP_TYPE_INVALID
- GROUP_OWNER_STORAGE_SIZE
- GROUPNAME_MAX_LENGTH
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a08efa37ad78fa3351d12fa43491c7b62ee64af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339582"
---
# <a name="cache-group-constants"></a>Cache Gruppen Konstanten

Die folgende Liste enthält die Konstanten, die von den Cache Gruppenfunktionen verwendet werden.

<dl> <dt>

<span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**cachegroup- \_ Attribut \_ Basic**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Ruft die Attribute "Flags", "Type" und "Disk Quota" der Cache Gruppe ab. Diese wird von der [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) -Funktion verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**cachegroup \_ - \_ attributflag**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Legt die der Cache Gruppe zugeordneten Flags fest oder ruft Sie ab. Diese wird von den Funktionen " [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) " und " [**lturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) " verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**cachegroup- \_ Attribut \_ get \_ all**
</dt> <dd> <dl> <dt>

0xFFFFFFFF
</dt> <dt>



Ruft alle Attribute der Cache Gruppe ab. Diese wird von der [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) -Funktion verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**cachegroup- \_ Attribut \_ Gruppenname**
</dt> <dd> <dl> <dt>

0x000000010
</dt> <dt>



Legt den Gruppennamen der Cache Gruppe fest oder ruft ihn ab. Diese wird von den Funktionen " [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) " und " [**lturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) " verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**cachegroup- \_ Attribut \_ Kontingent**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Legt das der Cache Gruppe zugeordnete Datenträger Kontingent fest oder ruft es ab. Diese wird von den Funktionen " [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) " und " [**lturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) " verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**cachegroup- \_ Attribut \_ Speicher**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Legt den Gruppenbesitzer Speicher fest, der der Cache Gruppe zugeordnet ist, oder ruft ihn ab. Diese wird von den Funktionen " [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) " und " [**lturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) " verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**cachegroup \_ - \_ Attributtyp**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Legt den Cache Gruppentyp fest oder ruft ihn ab. Diese wird von den Funktionen " [**geturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) " und " [**lturlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) " verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**cachegroup- \_ Flag \_ flushurl \_ OnDelete**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Gibt an, dass alle der Cache Gruppe zugeordneten Cache Einträge gelöscht werden sollen, es sei denn, der Eintrag gehört zu einer anderen Cache Gruppe.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**cachegroup- \_ Flag " \_ gidonly"**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Gibt an, dass die Funktion nur eine eindeutige GroupID für die Cache Gruppe erstellen und nicht die tatsächliche Gruppe erstellen soll.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**cachegroup- \_ Flag ist \_ nicht ersetzbar**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Gibt an, dass die Cache Gruppe nicht gelöscht werden kann.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**cachegroup- \_ Lese Schreib \_ Maske**
</dt> <dd> <dl> <dt>

0x0000003c
</dt> <dt>



Legt den Typ, das Datenträger Kontingent, den Gruppennamen und die Besitzer Speicher Attribute der Cache Gruppe fest. Diese wird von der Funktion " [**setlcachegroupattribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) " verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**cachegroup- \_ Suche \_ alle**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Gibt an, dass alle Cache Gruppen im System des Benutzers aufgezählt werden sollen.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**cachegroup \_ - \_ suchbyurl**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Derzeit nicht implementiert.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**cachegroup- \_ Typ ist \_ ungültig.**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Gibt an, dass der Cache Gruppentyp ungültig ist.


</dt> </dl> </dd> <dt>

<span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**\_ \_ Speicher \_ Größe des Gruppen Besitzers**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Länge des Gruppenbesitzer-Speicherarrays.


</dt> </dl> </dd> <dt>

<span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**\_Maximale Länge für GroupName \_**
</dt> <dd> <dl> <dt>

0x00000078
</dt> <dt>



Maximale Anzahl von Zeichen, die für einen Cache Gruppennamen zulässig sind.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



 

