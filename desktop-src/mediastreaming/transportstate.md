---
title: Transportstate-Enumeration
description: Definiert die verfügbaren Transport Zustände gemäß den UPnP-Richtlinien.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- Transportstate-Enumeration Medien Streaming-API
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
ms.openlocfilehash: 865d7e0f6a96727915833bb402860cde661162f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358769"
---
# <a name="transportstate-enumeration"></a>Transportstate-Enumeration

Definiert die verfügbaren Transport Zustände gemäß den UPnP-Richtlinien.

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

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannter**
</dt> <dd>

Fehlerhafter Gerätezustand.

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Abgeh**
</dt> <dd>

Der Transport des Geräts wurde beendet.

</dd> <dt>

<span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Ens**
</dt> <dd>

Der Transport des Geräts befindet sich im Zustand "Wiedergabe".

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang**
</dt> <dd>

Der Transport des Geräts befindet sich in einem Übergangszustand, der zu einem anderen Statuswert führt.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angehalten**
</dt> <dd>

Der Transport des Geräts befindet sich im angehaltenen Zustand.

</dd> <dt>

<span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Verzeichnet**
</dt> <dd>

Der Transport des Geräts ist in einem Aufzeichnungs Zustand.

</dd> <dt>

<span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**Nomediapresent**
</dt> <dd>

Für den Transport des Geräts ist kein URI für die Wiedergabe festgelegt.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Letzten**
</dt> <dd>

Der vorherige Zustand des Geräts zum aktuellen Transportzustand.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. Streaming. idl (Referenz zu Windows. Media. Streaming. idl)</dt> </dl> |



 

 





