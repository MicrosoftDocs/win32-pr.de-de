---
title: ControlReconnectStatus-Enumeration
description: Gibt das Ergebnis der IMsRdpClient8 Reconnect-Methode an.
ms.assetid: FB0AC4CF-18F5-4CDD-A75C-59A7CF716688
ms.tgt_platform: multiple
keywords:
- ControlReconnectStatus-Enumerations Remotedesktopdienste
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
ms.openlocfilehash: 635adbcafd5180dad967e2488b793f6907fd38cc848935a088bee59aad536354
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738080"
---
# <a name="controlreconnectstatus-enumeration"></a>ControlReconnectStatus-Enumeration

Gibt das Ergebnis der [**IMsRdpClient8::Reconnect-Methode**](imsrdpclient8-reconnect.md) an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  controlReconnectStarted  = 0x0000,
  controlReconnectBlocked  = 0x0001
} ControlReconnectStatus;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**
</dt> <dd>

Der Vorgang zum Wiederherstellen der Verbindung wurde gestartet.

</dd> <dt>

<span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**
</dt> <dd>

Der Vorgang zum Wiederherstellen der Verbindung konnte nicht gestartet werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md)
</dt> </dl>

 

 





