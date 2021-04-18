---
description: Der WPD-Vorgang gibt an, dass \_ \_ Enumerationswerte den aktuellen Status eines aktuell ausgeführten Vorgangs beschreiben.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: WPD_OPERATION_STATES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1746ab6a798c74974708ac10b9c4d137bf6c1d42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361372"
---
# <a name="wpd_operation_states-enumeration"></a>WPD- \_ Operation \_ States-Enumeration

Der **WPD \_ - \_ Vorgang** gibt an, dass Enumerationswerte den aktuellen Status eines aktuell ausgeführten Vorgangs beschreiben.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**der WPD- \_ Vorgangs \_ Status ist \_ nicht angegeben.**
</dt> <dd>

Der aktuelle Vorgang befindet sich in einem nicht angegebenen Zustand (nicht festgelegt) und ist unbekannt.

</dd> <dt>

<span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**WPD- \_ Vorgangs \_ Status wurde \_ gestartet.**
</dt> <dd>

Der Vorgang wird gestartet.

</dd> <dt>

<span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**WPD- \_ Vorgangs \_ Status wird \_ ausgeführt**
</dt> <dd>

Der Vorgang wird ausgeführt.

</dd> <dt>

<span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**WPD- \_ Vorgangs \_ Status \_ angehalten**
</dt> <dd>

Der Vorgang wurde angehalten.

</dd> <dt>

<span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**WPD- \_ Vorgangs \_ Status \_ abgebrochen**
</dt> <dd>

Der Vorgang wird abgebrochen.

</dd> <dt>

<span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**WPD- \_ Vorgangs \_ Status \_ abgeschlossen**
</dt> <dd>

Der Vorgang ist abgeschlossen.

</dd> <dt>

<span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**WPD- \_ Vorgangs \_ Status \_ abgebrochen**
</dt> <dd>

Der Vorgang wird abgebrochen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Werte werden im Anwendungs definierten Rückruf ([**iportabledeviceeventcallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)) empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




