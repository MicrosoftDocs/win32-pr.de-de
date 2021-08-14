---
description: Die EXPERTCONFIG-Struktur enthält die Konfigurationsdaten des Experten. Der Experte überlagert das RawConfigData-Element mit einer expertenspezifischen Struktur.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: EXPERTCONFIG-Struktur (Netmon.h)
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
ms.openlocfilehash: 93b47054fd5b8103d5bbe0d762db87f285a5f01690d0b93f6da14d215e404a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366910"
---
# <a name="expertconfig-structure"></a>EXPERTCONFIG-Struktur

Die **EXPERTCONFIG-Struktur** enthält die Konfigurationsdaten des Experten. Der Experte überlagert **das RawConfigData-Element** mit einer expertenspezifischen Struktur.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a>Member

<dl> <dt>

**RawConfigLength**
</dt> <dd>

Gesamtlänge der Struktur, einschließlich der vier Bytes, die für den Member verwendet werden. Netzwerkmonitor verwendet den -Wert, wenn die -Struktur auf einem Laufwerk gespeichert und von diesem gelesen wird.

</dd> <dt>

**RawConfigData**
</dt> <dd>

Konfigurationsdaten. Der Experte muss die Konfigurationsdaten hinzufügen. Angenommen, Sie verfügen über eine Datenstruktur, die wie diese aussieht.

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

Beachten Sie, **dass RawConfigLength sicherstellt,** dass die Überlagerung ordnungsgemäß funktioniert. Wenn Sie die Daten verwenden, könnte Ihr Code wie im folgenden Beispiel aussehen:

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
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




