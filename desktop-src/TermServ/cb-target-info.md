---
title: CB_TARGET_INFO-Struktur (Cbclient.h)
description: Enthält Informationen über den Zielcomputer und die IP-Adressen, an die eingehende Verbindungen umgeleitet werden sollen.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- CB_TARGET_INFO struktur Remotedesktopdienste
- PCB_TARGET_INFO strukturzeiger Remotedesktopdienste
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
ms.openlocfilehash: 1e7c00e1997ee36b42b21b833942597d9b43f393b2bcdfcee1aa0ee18e3a4548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001608"
---
# <a name="cb_target_info-structure"></a>CB \_ TARGET \_ INFO-Struktur

Enthält Informationen über den Zielcomputer und die IP-Adressen, an die eingehende Verbindungen umgeleitet werden sollen. Diese Struktur wird mit der [**IConnectionBrokerClient::GetTargetInfo-Methode**](iconnectionbrokerclient-gettargetinfo.md) verwendet.

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

Stellt den vollqualifizierten Domänennamen des Zielservers dar. Für ein RDV-Szenario (Remotedesktop Virtualization) ist dieser Member **NULL.** Für ein RDSH-Szenario (Remotedesktop Session Host) enthält dieses Mitglied den Servernamen, an den die eingehende Verbindung umgeleitet wird.

</dd> <dt>

**AddressCount**
</dt> <dd>

Die Anzahl gültiger Einträge im **Addresses-Array.**

</dd> <dt>

**Adresses**
</dt> <dd>

Ein Array von Zeichenfolgen, die die IP-Adressen enthalten, an die die eingehenden Verbindungen umgeleitet werden. Die Anzahl gültiger Elemente in diesem Array wird im **AddressCount-Member** angegeben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





