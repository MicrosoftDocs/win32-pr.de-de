---
title: TransportState-Enumeration
description: Definiert die verfügbaren Transportzustände gemäß den UPnP-Richtlinien.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- Media Streaming-API der TransportState-Enumeration
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a21fc8d0f2799cfba734d605d0c4d2835744ddeb130327ea39a22090d13464f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663090"
---
# <a name="transportstate-enumeration"></a>TransportState-Enumeration

Definiert die verfügbaren Transportzustände gemäß den UPnP-Richtlinien.

## <a name="syntax"></a>Syntax


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt**
</dt> <dd>

Fehlerhafter Gerätezustand.

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Gestoppt**
</dt> <dd>

Der Transport des Geräts befindet sich in einem angehaltenen Zustand.

</dd> <dt>

<span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Spielen**
</dt> <dd>

Der Transport des Geräts befindet sich im Wiedergabezustand.

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang**
</dt> <dd>

Der Transport des Geräts befindet sich in einem Übergangszustand, der zu einem anderen Zustandswert führt.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angehalten**
</dt> <dd>

Der Transport des Geräts befindet sich in einem angehaltenen Zustand.

</dd> <dt>

<span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Aufnahme**
</dt> <dd>

Der Transport des Geräts befindet sich in einem Aufzeichnungszustand.

</dd> <dt>

<span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**
</dt> <dd>

Für den Gerätetransport ist kein URI für die Wiedergabe festgelegt.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**letzte**
</dt> <dd>

Der vorherige Zustand des Geräts in den aktuellen Transportzustand.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Windows. Media.Streaming.idl (Referenz Windows. Media.Streaming.idl)</dt> </dl> |



 

 





