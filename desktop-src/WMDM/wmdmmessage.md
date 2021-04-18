---
title: Wmdmmess-Enumeration
description: Der wmdmmess-Enumerationstyp definiert Nachrichten Typen und-Zustände.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- Wmdmmess-Enumeration Windows Media Device Manager
topic_type:
- apiref
api_name:
- WMDMMessage
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489dc7059f10e1a6f61d1a290f8f664a385f96c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364447"
---
# <a name="wmdmmessage-enumeration"></a>Wmdmmess-Enumeration

Der **wmdmmess** -Enumerationstyp definiert Nachrichten Typen und-Zustände.

## <a name="syntax"></a>Syntax


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**WMDM-Meldung \_ \_ Geräte \_ Ankunft**
</dt> <dd>

Ein Windows Media Device Manager-Gerät wurde angeschlossen.

</dd> <dt>

<span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**WMDM-Meldung \_ \_ Geräte \_ Entfernung**
</dt> <dd>

Ein Windows Media Device Manager-Gerät wurde entfernt.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**WMDM- \_ msg- \_ Medien \_ Ankunft**
</dt> <dd>

Medien wurden in ein Windows Media Device Manager-Gerät eingefügt.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**Entfernen von WMDM- \_ msg- \_ Medien \_**
</dt> <dd>

Das Medium wurde von einem Windows Media Device Manager-Gerät entfernt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





