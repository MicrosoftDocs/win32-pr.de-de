---
title: Transportstatus-Enumeration
description: Definiert den verfügbaren Transport Status gemäß den UPnP-Richtlinien.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- Transportstatus-Enumeration Medien Streaming-API
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
ms.openlocfilehash: bb4a9de34f358db96b468dbd3329483a8e09b6b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362129"
---
# <a name="transportstatus-enumeration"></a>Transportstatus-Enumeration

Definiert den verfügbaren Transport Status gemäß den UPnP-Richtlinien.

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

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannter**
</dt> <dd>

Fehlerhafter Gerätestatus.

</dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Okay**
</dt> <dd>

Das Gerät befindet sich in einem guten Status.

</dd> <dt>

<span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**Fehler aufgetreten**
</dt> <dd>

Auf dem Gerät ist ein Fehler aufgetreten.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Letzten**
</dt> <dd>

Der vorherige Status des Geräts zum aktuellen Transport Status.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. Streaming. idl (Referenz zu Windows. Media. Streaming. idl)</dt> </dl> |



 

 





