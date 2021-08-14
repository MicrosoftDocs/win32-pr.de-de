---
title: MPDETECTION_STATE -Enumeration (MpClient.h)
description: Der Status der derzeit erkannten Bedrohung.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE enumeration Legacy Windows Environment Features
- PMPDETECTION_STATE-Enumerationszeiger Legacy Windows Umgebungsfeatures
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
ms.openlocfilehash: 0443e0c47eef4d4943d39bd671c28c19db0ff5e1fbe79e5af8d034603b1ab78d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883517"
---
# <a name="mpdetection_state-enumeration"></a>MPDETECTION \_ STATE-Enumeration

Der Status der derzeit erkannten Bedrohung.

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

<span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**MPDETECTION \_ STATE \_ UNKNOWN**
</dt> <dd>

In einem Fehlerzustand.

</dd> <dt>

<span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**MPDETECTION \_ STATE \_ ACTIVE**
</dt> <dd>

Aktive Bedrohung.

</dd> <dt>

<span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**MPDETECTION-STATUS \_ \_ ABGESCHLOSSEN**
</dt> <dd>

Ausstehende 24 Stunden bis zu einer Zusendung.

</dd> <dt>

<span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**MPDETECTION STATE ADDITIONAL ACTIONS (ZUSÄTZLICHE \_ \_ AKTIONEN ZUM MPDETECTION-ZUSTAND) \_**
</dt> <dd>

Zusätzliche Aktionen sind erforderlich.

</dd> <dt>

<span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**FEHLER BEIM \_ MPDETECTION-ZUSTAND \_**
</dt> <dd>

Nicht kritischer Korrekturfehler.

</dd> <dt>

<span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**MPDETECTION \_ STATE \_ CRITICALLY \_ FAILED**
</dt> <dd>

Kritischer Korrekturfehler.

</dd> <dt>

<span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**MPDETECTION \_ STATE \_ CLEARED**
</dt> <dd>

Die Bedrohung wird nicht in der Zustandsabfrage angezeigt, sondern nur im Verlauf.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





