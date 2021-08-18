---
title: Bindungstime out-Konstanten (Rpcdce.h)
description: Die RPC-Bibliothek verwendet die Time out-Konstanten für die Bindung, um die relative Zeitspanne anzugeben, die zum Einrichten einer Bindung an den Server aufgewendet werden soll, bevor sie aufgibt.
ms.assetid: bf5f3f08-ab29-4732-9ce3-d6d7ad699369
topic_type:
- apiref
api_name:
- RPC_C_BINDING_INFINITE_TIMEOUT
- RPC_C_BINDING_MIN_TIMEOUT
- RPC_C_BINDING_DEFAULT_TIMEOUT
- RPC_C_BINDING_MAX_TIMEOUT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 125a38dd41445ba0661d13c61e7c79e689bc29abffa535791b233c40cfb704ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932361"
---
# <a name="binding-time-out-constants"></a>Binden von Time out-Konstanten

Die RPC-Bibliothek verwendet die Time out-Konstanten für die Bindung, um die relative Zeitspanne anzugeben, die zum Einrichten einer Bindung an den Server aufgewendet werden soll, bevor sie aufgibt. Das Timeout kann mit einem Aufruf der [**RpcMgmtSetComTimeout-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) aktiviert werden. Die folgende Liste enthält die gültigen Time out-Werte.



| Konstante/Wert                                                                                                                                                                                                                                                                | Beschreibung                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <dt>**RPC \_ C \_ BINDING \_ INFINITE \_ TIMEOUT**</dt> <dt> 10</dt> </dl> | Versucht ständig, die Kommunikation dauerhaft einzurichten.<br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <dt>**RPC \_ C \_ BINDUNG \_ MIN \_ TIMEOUT**</dt> <dt>0</dt> </dl>                   | Versucht, die Mindestzeit für das verwendete Netzwerkprotokoll zu verwenden. Dieser Wert bevorzugt die Antwortzeit gegenüber der Korrektheit bei der Bestimmung, ob der Server ausgeführt wird.<br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <dt>**RPC \_ \_ \_ \_ STANDARDTIMEOUT FÜR C-BINDUNG**</dt> <dt>5</dt> </dl>       | Versucht eine durchschnittliche Zeitspanne für das verwendete Netzwerkprotokoll. Dieser Wert gibt Korrektheit bei der Bestimmung, ob ein Server ausgeführt wird, und gibt der Antwortzeit die gleiche Gewichtung. Dies ist der Standardwert.<br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <dt>**RPC \_ \_C BINDING MAX \_ \_ TIMEOUT**</dt> <dt>9</dt> </dl>                   | Versucht die längste Zeitspanne für das verwendete Netzwerkprotokoll. Dieser Wert bevorzugt die Richtigkeit bei der Bestimmung, ob ein Server während der Antwortzeit ausgeführt wird.<br/>                                            |



## <a name="remarks"></a>Hinweise

Die Werte in der obigen Tabelle sind nicht in Sekunden. Diese Werte stellen einen relativen Zeitraum auf einer Skala von 0 bis 10 dar. Weitere Informationen zum Vermeiden von Kommunikationsverzögerungen finden Sie unter Verhindern von clientseitigen Hängen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Rpcdce.h</dt> </dl> |



 

 





