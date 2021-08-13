---
description: Die WPD \_ OPERATION \_ STATES-Enumerationswerte beschreiben den aktuellen Zustand eines ausgeführten Vorgangs.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: WPD_OPERATION_STATES-Enumeration (PortableDevice.h)
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
ms.openlocfilehash: 3c2bc25fdbc040bd849d60f1e16e5d86d1916ced17eb6670ceb3bc6a75108772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696483"
---
# <a name="wpd_operation_states-enumeration"></a>WPD \_ OPERATION \_ STATES-Enumeration

Die **WPD \_ OPERATION \_ STATES-Enumerationswerte** beschreiben den aktuellen Zustand eines ausgeführten Vorgangs.

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

<span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**\_WPD-VORGANGSSTATUS \_ \_ NICHT ANGEGEBEN**
</dt> <dd>

Der aktuelle Vorgang befindet sich in einem nicht angegebenen Zustand (nicht festgelegt) und unbekannt.

</dd> <dt>

<span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**\_WPD-VORGANGSSTATUS \_ \_ GESTARTET**
</dt> <dd>

Der Vorgang wird gestartet.

</dd> <dt>

<span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**\_WPD-VORGANGSSTATUS \_ \_ WIRD AUSGEFÜHRT**
</dt> <dd>

Der Vorgang wird ausgeführt.

</dd> <dt>

<span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**\_WPD-VORGANGSSTATUS \_ \_ ANGEHALTEN**
</dt> <dd>

Der Vorgang wird angehalten.

</dd> <dt>

<span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**\_WPD-VORGANGSSTATUS \_ \_ ABGEBROCHEN**
</dt> <dd>

Der Vorgang wird abgebrochen.

</dd> <dt>

<span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**\_WPD-VORGANGSSTATUS \_ \_ ABGESCHLOSSEN**
</dt> <dd>

Der Vorgang ist abgeschlossen.

</dd> <dt>

<span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**\_WPD-VORGANGSSTATUS \_ \_ ABGEBROCHEN**
</dt> <dd>

Der Vorgang wird abgebrochen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Werte werden im anwendungsdefinierte Rückruf empfangen ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




