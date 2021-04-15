---
title: MPDETECTION_STATE-Enumeration (mpclient. h)
description: Der Status der aktuell erkannten Bedrohung.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPDETECTION_STATE enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPDETECTION_STATE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9265a15641d2072d87b33af2782f17974bf07be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476113"
---
# <a name="mpdetection_state-enumeration"></a>Mperkennungs- \_ statusenumeration

Der Status der aktuell erkannten Bedrohung.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPDETECTION_STATE { 
  MPDETECTION_STATE_UNKNOWN             = 0,
  MPDETECTION_STATE_ACTIVE              = 1,
  MPDETECTION_STATE_FINISHED            = 2,
  MPDETECTION_STATE_ADDITIONAL_ACTIONS  = 3,
  MPDETECTION_STATE_FAILED              = 4,
  MPDETECTION_STATE_CRITICALLY_FAILED   = 5,
  MPDETECTION_STATE_CLEARED             = 6
} MPDETECTION_STATE, *PMPDETECTION_STATE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**Unbekannter mperkennungs- \_ Zustand. \_**
</dt> <dd>

In einem Fehlerzustand.

</dd> <dt>

<span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**mperkennungs- \_ Status \_ aktiv**
</dt> <dd>

Aktive Bedrohung.

</dd> <dt>

<span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**mperkennungs- \_ Status \_ abgeschlossen**
</dt> <dd>

Ausstehende 24 Stunden bis zum Löschen.

</dd> <dt>

<span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**mperkennungs \_ Status \_ zusätzliche \_ Aktionen**
</dt> <dd>

Weitere erforderliche Aktionen.

</dd> <dt>

<span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**mperkennungs- \_ Status ist \_ fehlgeschlagen**
</dt> <dd>

Nicht schwerwiegender Fehler bei der Wiederherstellung.

</dd> <dt>

<span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**Fehler beim mperkennungs \_ Zustand. \_ \_**
</dt> <dd>

Kritischer Fehler bei der Wiederherstellung.

</dd> <dt>

<span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**mperkennungs- \_ Status \_ gelöscht**
</dt> <dd>

Die Bedrohung wird in der Zustands Abfrage nicht angezeigt, sondern nur im Verlauf.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





