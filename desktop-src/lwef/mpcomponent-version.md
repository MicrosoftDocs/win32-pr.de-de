---
title: MPCOMPONENT_VERSION Struktur (mpclient. h)
description: Versions-und Aktualisierungszeit für eine einzelne Komponente.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- MPCOMPONENT_VERSION Struktur Funktionen der Legacy-Windows-Umgebung
- PMPCOMPONENT_VERSION Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1d4b5011bb185dc8ca0892e0a0e65bc4a7d8b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949824"
---
# <a name="mpcomponent_version-structure"></a>Mpcomponent- \_ Versions Struktur

Versions-und Aktualisierungszeit für eine einzelne Komponente.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a>Member

<dl> <dt>

**Version**
</dt> <dd>

Typ: **ULONGLONG**

</dd> <dd>

Versions Feld. Jedes **Wort** stellt die Haupt-, neben Version, Build und Revision dar.

</dd> <dt>

**Update time**
</dt> <dd>

Typ: **ularge \_ Integer**

</dd> <dd>

Der Zeitpunkt der letzten Aktualisierung der Komponente im **FILETIME** -Format.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





