---
title: TransportStatus-Enumeration
description: Definiert den verfügbaren Transportstatus gemäß den UPnP-Richtlinien.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- TransportStatus-Enumerations-Medienstreaming-API
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96b7d3892d0344b166665426c66313da370aed1abbdb80c17037ea6aeb44e46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472996"
---
# <a name="transportstatus-enumeration"></a>TransportStatus-Enumeration

Definiert den verfügbaren Transportstatus gemäß den UPnP-Richtlinien.

## <a name="syntax"></a>Syntax


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt**
</dt> <dd>

Fehlerhafter Gerätestatus.

</dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Okay**
</dt> <dd>

Das Gerät befindet sich in einem guten Status.

</dd> <dt>

<span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**
</dt> <dd>

Auf dem Gerät ist ein Fehler aufgetreten.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**letzte**
</dt> <dd>

Der vorherige Status des Geräts ist der aktuelle Transportstatus.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Windows. Media.Streaming.idl (Referenz Windows. Media.Streaming.idl)</dt> </dl> |



 

 





