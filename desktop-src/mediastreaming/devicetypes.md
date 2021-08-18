---
title: DeviceTypes-Enumeration
description: Beschreibt die DLNA-Gerätetypen, die von der Medienstreaming-API unterstützt werden.
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- Media Streaming-API für DeviceTypes-Enumeration
topic_type:
- apiref
api_name:
- DeviceTypes
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969eb389a1216ec0e30f27a938ca4f5382397ac5489f87add87731b69824b87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100654"
---
# <a name="devicetypes-enumeration"></a>DeviceTypes-Enumeration

Beschreibt die DLNA-Gerätetypen, die von der Medienstreaming-API unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum DeviceTypes { 
  Unknown               = 0x0,
  DigitalMediaRenderer  = 0x1,
  DigitalMediaServer    = 0x2,
  DigitalMediaPlayer    = 0x4
} DeviceTypes;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt**
</dt> <dd>

Unbekannter Gerätetyp.

</dd> <dt>

<span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**
</dt> <dd>

DLNA Digital Media Renderer (DMR). Der Wert entspricht dem Gerätetyp **urn:schemas-upnp-org:device:MediaRenderer:1**.

</dd> <dt>

<span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**
</dt> <dd>

DLNA Digital Media Server (DMS). Der Wert entspricht dem Gerätetyp **urn:schemas-upnp-org:device:MediaServer:1**.

</dd> <dt>

<span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**
</dt> <dd>

DLNA Digital Media Player

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Windows. Media.Streaming.idl (Referenz Windows. Media.Streaming.idl)</dt> </dl> |



 

 





