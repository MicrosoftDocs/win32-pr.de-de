---
title: WMDMMessage-Enumeration
description: Der WMDMMessage-Enumerationstyp definiert Nachrichtentypen und -zustände.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- WMDMMessage-Enumeration windows Media Geräte-Manager
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
ms.openlocfilehash: 348092e079428e0b147d8143411cee7766365913115f968ed0e112b209383077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862660"
---
# <a name="wmdmmessage-enumeration"></a>WMDMMessage-Enumeration

Der **WMDMMessage-Enumerationstyp** definiert Nachrichtentypen und -zustände.

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

<span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**WMDM \_ MSG \_ DEVICE \_ ARRIVAL**
</dt> <dd>

Ein Windows Media Geräte-Manager gerät wurde angeschlossen.

</dd> <dt>

<span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**WMDM \_ MSG \_ DEVICE \_ REMOVAL**
</dt> <dd>

Ein Windows Media Geräte-Manager wurde entfernt.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**WMDM \_ MSG \_ MEDIA \_ ARRIVAL**
</dt> <dd>

Medien wurden in ein Mediengerät Windows Medien Geräte-Manager eingefügt.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**WMDM: \_ ENTFERNEN VON \_ MSG-MEDIEN \_**
</dt> <dd>

Medien wurden aus einem Mediengerät entfernt, Windows Medien Geräte-Manager wurden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> </dl>

 

 





