---
description: Die stationquery-Struktur enthält Informationen zu einem bestimmten Computer, der Netzwerkmonitor verwendet.
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: Stationquery-Struktur (Netmon. h)
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
ms.openlocfilehash: de76c4da7bc27d76c04aeeaa7a46d69134e411ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358824"
---
# <a name="stationquery-structure"></a>Stationquery-Struktur

Die **stationquery** -Struktur enthält Informationen zu einem bestimmten Computer, der Netzwerkmonitor verwendet.

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

Flags, die den aktuellen Status Netzwerkmonitor identifizieren.



| Wert                                                                                                                                                                                                                | Bedeutung                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <dt>**stationquery- \_ Flags \_ geladen**</dt> </dl>                   | Der Treiber wird geladen, aber der Kernel ist nicht.<br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <dt>**stationquery- \_ Flags werden \_ ausgeführt**</dt> </dl>                | Der Treiber ist geladen, aber es werden keine Daten erfasst.<br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <dt>**Aufzeichnen von stationquery- \_ Flags \_**</dt> </dl>          | Der Treiber ist aktiv an einer Erfassung beteiligt.<br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <dt>**Übertragung von stationquery- \_ Flags \_**</dt> </dl> | Dieses Flag ist veraltet.<br/>                       |



 

</dd> <dt>

**Bcdverminor**
</dt> <dd>

Die neben Versionsnummer der Netzwerkmonitor, die auf dem Computer installiert ist.

</dd> <dt>

**Bcdvermajor**
</dt> <dd>

Die Hauptversionsnummer der Netzwerkmonitor, die auf dem Computer installiert ist.

</dd> <dt>

**Lizenznummer**
</dt> <dd>

Software Lizenznummer.

</dd> <dt>

**MachineName**
</dt> <dd>

Der Name des Computer Herstellers, falls vorhanden.

</dd> <dt>

**UserName**
</dt> <dd>

Benutzername oder System Bezeichner.

</dd> <dt>

**Reserved**
</dt> <dd>

Für die zukünftige Verwendung reserviert.

</dd> <dt>

**Adapteraddress**
</dt> <dd>

NIC-Adresse

</dd> <dt>

**Wmachinename**
</dt> <dd>

Name des Unicode-Computers. Dieser Member gilt für Netzwerkmonitor 2,0 oder höher.

</dd> <dt>

**Wusername**
</dt> <dd>

Unicode-Benutzername. Dieser Member gilt für Netzwerkmonitor 2,0 oder höher.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein Array dieser Strukturen wird von der [QueryTable](querytable.md) -Struktur verwendet, um eine Liste der Computer bereitzustellen, die derzeit Netzwerkmonitor zum Erfassen von Daten verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[QueryTable](querytable.md)
</dt> </dl>

 

 




