---
description: Die STATIONQUERY-Struktur stellt Informationen zu einem bestimmten Computer mithilfe von Netzwerkmonitor.
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: STATIONQUERY-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a2e46f4c0d213091a3915b5310d7768a193d33e5ac3391fd3bc3c6781e32cb57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363056"
---
# <a name="stationquery-structure"></a>STATIONQUERY-Struktur

Die **STATIONQUERY-Struktur** stellt Informationen zu einem bestimmten Computer mithilfe von Netzwerkmonitor.

## <a name="syntax"></a>Syntax


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a>Member

<dl> <dt>

**Flags**
</dt> <dd>

Flags, die den aktuellen Zustand der Netzwerkmonitor.



| Wert                                                                                                                                                                                                                | Bedeutung                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <dt>**GELADENE \_ \_ STATIONQUERY-FLAGS**</dt> </dl>                   | Der Treiber wird geladen, der Kernel jedoch nicht.<br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <dt>**\_STATIONQUERY-FLAGS \_ WERDEN AUSGEFÜHRT**</dt> </dl>                | Der Treiber wird geladen, erfasst aber keine Daten.<br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <dt>**ERFASSEN VON \_ STATIONQUERY-FLAGS \_**</dt> </dl>          | Der Treiber ist aktiv an einer Erfassung beteiligt.<br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <dt>**\_STATIONQUERY-FLAGS, \_ DIE ÜBERTRAGEN**</dt> </dl> | Dieses Flag ist veraltet.<br/>                       |



 

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

Nebenversionsnummer der Netzwerkmonitor auf dem Computer installiert.

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

Hauptversionsnummer der Netzwerkmonitor auf dem Computer installiert.

</dd> <dt>

**LicenseNumber**
</dt> <dd>

Softwarelizenznummer.

</dd> <dt>

**MachineName**
</dt> <dd>

Name des Computerherstellers, sofern eins vor ist.

</dd> <dt>

**UserName**
</dt> <dd>

Benutzername oder Systembezeichner.

</dd> <dt>

**Reserved**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**AdapterAddress**
</dt> <dd>

NIC-Adresse.

</dd> <dt>

**WMachineName**
</dt> <dd>

Unicode-Computername. Dieser Member gilt für Netzwerkmonitor 2.0 oder höher.

</dd> <dt>

**WUserName**
</dt> <dd>

Unicode-Benutzername. Dieser Member gilt für Netzwerkmonitor 2.0 oder höher.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Array dieser Strukturen wird von der [QUERYTABLE-Struktur](querytable.md) verwendet, um eine Liste der Computer zur Verfügung zu stellen, die Netzwerkmonitor zum Erfassen von Daten verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Querytable](querytable.md)
</dt> </dl>

 

 




