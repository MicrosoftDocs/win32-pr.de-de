---
description: Enthält die Tabelle mit Schlüsselinformationen für alle drahtlosen LAN-Schnittstellen, die vom drahtlos Konfigurations Dienst verwaltet werden.
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: INTFS_KEY_TABLE Struktur (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 4ef38f2317c763eaa6c7e0379be5c8b00c0ed6b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350473"
---
# <a name="intfs_key_table-structure"></a>Intfs- \_ Schlüssel \_ Tabellenstruktur

\[**Intfs \_ Die Schlüssel \_ Tabelle** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt. Verwenden Sie stattdessen die [native WiFi-API](native-wifi-reference.md), die eine ähnliche Funktionalität bietet. Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]

Die **intfs- \_ Schlüssel \_ Tabellen** Struktur enthält die Tabelle mit Schlüsselinformationen für alle drahtlosen LAN-Schnittstellen, die vom drahtlos Konfigurations Dienst verwaltet werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**dwnumintfs**
</dt> <dd>

Die Gesamtanzahl der Schnittstellen.

</dd> <dt>

**pintfs**
</dt> <dd>

Ein Zeiger auf die [**INTF- \_ Schlüssel \_ Eintrags**](intf-key-entry.md) Struktur.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei " *wzcsapi. h* " ist im Windows SDK nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Ende des Supports (Client)<br/>    | Windows XP mit SP3<br/>                                                       |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



 

 




