---
title: MPENDOFLIFE_DATA Struktur (mpclient. h)
description: '\ 0034; Ende des Lebenszyklus \ 0034; Benachrichtigungs Daten.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- MPENDOFLIFE_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPENDOFLIFE_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e209b9b35a089523815c353e8a750152bf4af75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104852"
---
# <a name="mpendoflife_data-structure"></a>\_Mpendomelife-Datenstruktur

"Lebensdauer"-Benachrichtigungs Daten.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**ftsignatureablauf**
</dt> <dd>

Typ: **FILETIME**

</dd> <dd>

Zeitpunkt, zu dem die Signatur abläuft.

</dd> <dt>

**ftplatformexpiry**
</dt> <dd>

Typ: **FILETIME**

</dd> <dd>

Uhrzeit, zu der die Plattform abläuft.

</dd> <dt>

**fadminkontrollierten**
</dt> <dd>

Typ: **bool**

</dd> <dd>

True, wenn der Administrator die Richtlinie zur Anzeige der Benachrichtigung steuert. Wenn dieser Wert festgelegt ist, weist die Benutzeroberfläche an, die EOL-Benachrichtigung nicht anzuzeigen.

</dd> <dt>

**fendoflifeimpumdingorpast**
</dt> <dd>

Typ: **bool**

</dd> <dd>

True, wenn "Ende des Lebenszyklus" aussteht oder überschreitet. False gibt an, dass die Benutzeroberfläche und die Clients alle EOL-bezogenen Zustände löschen können.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





