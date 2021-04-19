---
title: Debug Type-Enumeration
description: Beschreibt die DLNA-Gerätetypen, die von der Media Streaming-API unterstützt werden.
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- Geräte-Streaming-API der Geräte-Enumeration
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
ms.openlocfilehash: 9caf60fa5736f9db442da5787746a49f71c61c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361262"
---
# <a name="devicetypes-enumeration"></a>Debug Type-Enumeration

Beschreibt die DLNA-Gerätetypen, die von der Media Streaming-API unterstützt werden.

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

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannter**
</dt> <dd>

Unbekannter Gerätetyp.

</dd> <dt>

<span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**Digitalmediarenderer**
</dt> <dd>

DLNA Digital Media-Renderer (DMR). Der Wert entspricht dem Gerätetyp **urn: Schemas-UPnP-org: Device: MediaRenderer: 1**.

</dd> <dt>

<span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**Digitalmediaserver**
</dt> <dd>

DLNA Digital Media-Server (DMS). Der Wert entspricht dem Gerätetyp **urn: Schemas-UPnP-org: Device: Mediaserver: 1**.

</dd> <dt>

<span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**Digitalmediaplayer**
</dt> <dd>

Digitaler DLNA-Media Player

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. Streaming. idl (Referenz zu Windows. Media. Streaming. idl)</dt> </dl> |



 

 





