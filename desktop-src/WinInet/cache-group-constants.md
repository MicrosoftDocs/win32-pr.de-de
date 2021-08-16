---
title: Cachegruppenkonst constants (Wininet.h)
description: Die folgende Liste enthält die Konstanten, die von den Cachegruppenfunktionen verwendet werden.
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
ms.openlocfilehash: cb79ae76d743ff4633f6d7f359f96906d2f60cc64c2c35ab2544ae80918721a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955620"
---
# <a name="cache-group-constants"></a>Cachegruppenkonst constants

Die folgende Liste enthält die Konstanten, die von den Cachegruppenfunktionen verwendet werden.

<dl> <dt>

<span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**\_CACHEGROUP-ATTRIBUT \_ BASIC**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Ruft die Flags, den Typ und die Datenträgerkontingentattribute der Cachegruppe ab. Dies wird von der [**GetUrlCacheGroupAttribute-Funktion**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**\_ \_ CACHEGROUP-ATTRIBUTFLAG**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Legt die flags fest, die der Cachegruppe zugeordnet sind, oder ruft sie ab. Dies wird von den [**Funktionen GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) und [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**\_CACHEGROUP-ATTRIBUT \_ GET \_ ALL**
</dt> <dd> <dl> <dt>

0xffffffff
</dt> <dt>



Ruft alle Attribute der Cachegruppe ab. Dies wird von der [**GetUrlCacheGroupAttribute-Funktion**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**\_ \_ CACHEGROUP-ATTRIBUTGRUPPENNAME**
</dt> <dd> <dl> <dt>

0x000000010
</dt> <dt>



Legt den Gruppennamen der Cachegruppe fest oder ruft sie ab. Dies wird von den [**Funktionen GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) und [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**\_CACHEGROUP-ATTRIBUTKONTINGENT \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Legt das Datenträgerkontingent fest, das der Cachegruppe zugeordnet ist, oder ruft es ab. Dies wird von den [**Funktionen GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) und [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**\_CACHEGROUP-ATTRIBUTSPEICHER \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Legt den der Cachegruppe zugeordneten Gruppenbesitzerspeicher fest oder ruft diesen ab. Dies wird von den [**Funktionen GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) und [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**\_CACHEGROUP-ATTRIBUTTYP \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Legt den Cachegruppentyp fest oder ruft diesen ab. Dies wird von den [**Funktionen GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) und [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**\_CACHEGROUP-FLAG \_ FLUSHURL \_ ONDELETE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Gibt an, dass alle Cacheeinträge, die der Cachegruppe zugeordnet sind, gelöscht werden sollen, es sei denn, der Eintrag gehört zu einer anderen Cachegruppe.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**\_CACHEGROUP-FLAG \_ GIDONLY**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Gibt an, dass die Funktion nur eine eindeutige GROUPID für die Cachegruppe und nicht die tatsächliche Gruppe erstellen soll.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**CACHEGROUP \_ FLAG \_ NONPURGEABLE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Gibt an, dass die Cachegruppe nicht gelöscht werden kann.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**CACHEGROUP \_ READWRITE \_ MASK**
</dt> <dd> <dl> <dt>

0x0000003c
</dt> <dt>



Legt den Typ, das Datenträgerkontingent, den Gruppennamen und die Speicherattribute des Besitzers der Cachegruppe fest. Dies wird von der [**SetUrlCacheGroupAttribute-Funktion**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) verwendet.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP \_ SEARCH \_ ALL**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Gibt an, dass alle Cachegruppen im System des Benutzers aufzählt werden sollen.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP \_ SEARCH \_ BYURL**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Derzeit nicht implementiert.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**\_CACHEGROUP-TYP \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Gibt an, dass der Cachegruppentyp ungültig ist.


</dt> </dl> </dd> <dt>

<span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**SPEICHERGRÖßE \_ DES \_ \_ GRUPPENBESITZERS**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Länge des Gruppenbesitzer-Speicherarrays.


</dt> </dl> </dd> <dt>

<span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**GROUPNAME \_ MAX \_ LENGTH**
</dt> <dd> <dl> <dt>

0x00000078
</dt> <dt>



Maximale Anzahl von Zeichen, die für einen Cachegruppennamen zulässig sind.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

> [!Note]  
> WinINet unterstützt keine Serverimplementierung. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



 

