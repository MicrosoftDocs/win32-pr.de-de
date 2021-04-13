---
title: CB_CONNECTION_INFO Struktur (cbclient. h)
description: Enthält Informationen über eine eingehende Verbindungsanforderung.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- CB_CONNECTION_INFO Struktur Remotedesktopdienste
- PCB_CONNECTION_INFO Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36370a4faa823f509d1f3356768add0ece9a6904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391689"
---
# <a name="cb_connection_info-structure"></a>CB- \_ Verbindungs \_ Informationsstruktur

Enthält Informationen über eine eingehende Verbindungsanforderung. Diese Struktur wird mit der [**iconnectionbrokerclient:: gettargetinfo**](iconnectionbrokerclient-gettargetinfo.md) -Methode verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**UserName**
</dt> <dd>

Der Name des Benutzers, der eine Sitzung anfordert.

</dd> <dt>

**Domäne**
</dt> <dd>

Der Name der Domäne, in der der **Benutzername** Mitglied ist.

</dd> <dt>

**InitialProgram**
</dt> <dd>

Der voll qualifizierte Pfad und Dateiname des ersten Programms, das beim Starten der Sitzung gestartet wird. Legen Sie diesen Member auf eine leere Zeichenfolge fest, wenn kein erstes Programm gestartet werden soll.

</dd> <dt>

**Ressource**
</dt> <dd>

Ein Wert der [**CB- \_ \_ Ressourcentyp**](cb-resource-type.md) Enumeration, die den Ressourcentyp angibt, mit dem die eingehende Verbindung eine Verbindung herstellt. Wenn der **PluginName** -Member **null** ist, wird dieser Member vom Remotedesktopverbindung Broker verwendet, um zu bestimmen, welches Plug-in zum Bestimmen des Ziel Computers aufgerufen werden soll.

</dd> <dt>

**PluginName**
</dt> <dd>

Der Name des Plug-ins, das zum Bestimmen des Ziel Computers aufgerufen werden soll. Wenn dieser Parameter **null** ist, wird das **Ressourcen** Element verwendet, um zu bestimmen, welches Plug-in aufgerufen werden soll.

</dd> <dt>

**Farmname**
</dt> <dd>

Der Name der Farm, die die Computer enthält, von denen einer der Zielcomputer ist, auf den die Verbindung umgeleitet wird.

</dd> <dt>

**dwvendorinfolength**
</dt> <dd>

Dieses Element ist für die zukünftige Verwendung reserviert.

</dd> <dt>

**pvendorspecificinfo**
</dt> <dd>

Dieses Element ist für die zukünftige Verwendung reserviert.

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

 

 





