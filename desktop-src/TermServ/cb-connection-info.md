---
title: CB_CONNECTION_INFO-Struktur (Cbclient.h)
description: Enthält Informationen zu einer eingehenden Verbindungsanforderung.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- CB_CONNECTION_INFO struktur Remotedesktopdienste
- PCB_CONNECTION_INFO Strukturzeiger Remotedesktopdienste
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
ms.openlocfilehash: 6fd433f668c178973a4e3690ea130d01d75fab79e739610f77ac00619b9e326c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575040"
---
# <a name="cb_connection_info-structure"></a>CB \_ CONNECTION \_ INFO-Struktur

Enthält Informationen zu einer eingehenden Verbindungsanforderung. Diese Struktur wird mit der [**IConnectionBrokerClient::GetTargetInfo-Methode**](iconnectionbrokerclient-gettargetinfo.md) verwendet.

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

**Domain**
</dt> <dd>

Der Name der Domäne, der **UserName** angehört.

</dd> <dt>

**InitialProgram**
</dt> <dd>

Der vollqualifizierte Pfad und Dateiname des ersten Programms, das beim Starten der Sitzung gestartet wird. Legen Sie diesen Member auf eine leere Zeichenfolge fest, wenn kein anfängliches Programm gestartet werden soll.

</dd> <dt>

**Ressource**
</dt> <dd>

Ein Wert der [**CB \_ RESOURCE \_ TYPE-Enumeration,**](cb-resource-type.md) der den Typ der Ressource angibt, mit der die eingehende Verbindung eine Verbindung herstellt. Wenn das **Plug-InName-Element** **NULL** ist, wird dieses Element vom Remotedesktopverbindung Broker verwendet, um zu bestimmen, welches Plug-In zum Bestimmen des Zielcomputers aufgerufen werden soll.

</dd> <dt>

**PluginName**
</dt> <dd>

Der Name des Plug-Ins, das aufgerufen werden soll, um den Zielcomputer zu bestimmen. Wenn dieser Parameter **NULL** ist, wird der **Ressourcenmember** verwendet, um zu bestimmen, welches Plug-In aufgerufen werden soll.

</dd> <dt>

**FarmName**
</dt> <dd>

Der Name der Farm, die die Computer enthält. Einer davon ist der Zielcomputer, auf den die Verbindung umgeleitet wird.

</dd> <dt>

**dwVendorInfoLength**
</dt> <dd>

Dieses Element ist für die zukünftige Verwendung reserviert.

</dd> <dt>

**pVendorSpecificInfo**
</dt> <dd>

Dieses Element ist für die zukünftige Verwendung reserviert.

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

 

 





