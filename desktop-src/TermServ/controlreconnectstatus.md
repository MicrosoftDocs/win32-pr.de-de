---
title: Controlreconnectstatus-Enumeration
description: Gibt das Ergebnis der IMsRdpClient8 Reconnect-Methode an.
ms.assetid: FB0AC4CF-18F5-4CDD-A75C-59A7CF716688
ms.tgt_platform: multiple
keywords:
- Controlreconnectstatus-Enumeration Remotedesktopdienste
topic_type:
- apiref
api_name:
- ControlReconnectStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5638cbdda268dd453881ee1d88085728479aada6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340981"
---
# <a name="controlreconnectstatus-enumeration"></a>Controlreconnectstatus-Enumeration

Gibt das Ergebnis der [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) -Methode an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  controlReconnectStarted  = 0x0000,
  controlReconnectBlocked  = 0x0001
} ControlReconnectStatus;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlreconnectstarted**
</dt> <dd>

Der Vorgang zum erneuten Verbinden wurde gestartet.

</dd> <dt>

<span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlreconnectblockierte**
</dt> <dd>

Der Vorgang zum erneuten Verbinden konnte nicht gestartet werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md)
</dt> </dl>

 

 





