---
title: CB_TARGET_INFO Struktur (cbclient. h)
description: Enthält Informationen über den Zielcomputer und die IP-Adressen, an die eingehende Verbindungen umgeleitet werden sollen.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- CB_TARGET_INFO Struktur Remotedesktopdienste
- PCB_TARGET_INFO Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bbb982636449075b758ac61178f5e97da47ce7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391688"
---
# <a name="cb_target_info-structure"></a>CB- \_ Ziel \_ Informationsstruktur

Enthält Informationen über den Zielcomputer und die IP-Adressen, an die eingehende Verbindungen umgeleitet werden sollen. Diese Struktur wird mit der [**iconnectionbrokerclient:: gettargetinfo**](iconnectionbrokerclient-gettargetinfo.md) -Methode verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**ServerName**
</dt> <dd>

Stellt den voll qualifizierten Domänen Namen des Zielservers dar. Bei einem Remotedesktop Virtualisierungsszenario (RDV) ist dieser Member **null**. Bei einem Remotedesktop-Sitzungs Host Szenario (RDSH) enthält dieser Member den Namen des Servers, auf den die eingehende Verbindung umgeleitet wird.

</dd> <dt>

**Addresscount**
</dt> <dd>

Die Anzahl der gültigen Einträge im **Adress** Array.

</dd> <dt>

**Adresses**
</dt> <dd>

Ein Array von Zeichen folgen, die die IP-Adressen enthalten, an die die eingehenden Verbindungen umgeleitet werden. Die Anzahl der gültigen Elemente in diesem Array wird im **addresscount** -Member angegeben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconnectionbrokerclient:: gettargetinfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





