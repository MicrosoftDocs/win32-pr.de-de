---
description: Die Struktur "expertconfig" enthält die Konfigurationsdaten des Experten. Der Experte überlagert den rawConfigData-Member mit einer expertenspezifischen Struktur.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: Expertenconfig-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 293bdf4c792c10232564a7ba6386df430e81ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342822"
---
# <a name="expertconfig-structure"></a>Expertenkonfigurations-Struktur

Die Struktur " **expertconfig** " enthält die Konfigurationsdaten des Experten. Der Experte überlagert den **rawConfigData** -Member mit einer expertenspezifischen Struktur.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a>Member

<dl> <dt>

**Rawconfiglength**
</dt> <dd>

Gesamtlänge der Struktur, einschließlich der vier Bytes, die für den Member verwendet werden. Netzwerkmonitor verwendet den-Wert, wenn die Struktur in einem Laufwerk gespeichert und von diesem gelesen wird.

</dd> <dt>

**RawConfigData**
</dt> <dd>

Konfigurationsdaten. Der Experte muss die Konfigurationsdaten hinzufügen. Angenommen, Sie verfügen über eine Datenstruktur, die wie folgt aussieht.

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

Beachten Sie, dass **rawconfiglength** sicherstellt, dass das Overlay ordnungsgemäß funktioniert. Wenn Sie die Daten verwenden, könnte Ihr Code wie folgt aussehen:

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




