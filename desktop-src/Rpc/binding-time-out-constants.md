---
title: Bindungs Timeout Konstanten (rpcdce. h)
description: Die RPC-Bibliothek verwendet die Bindungs Timeout Konstanten, um die relative Zeitspanne anzugeben, die für das Herstellen einer Bindung an den Server aufgewendet werden soll, bevor ein Timeout auftritt.
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
ms.openlocfilehash: d096fd320e1341f9affc35ae6ff1d355fcf12d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337727"
---
# <a name="binding-time-out-constants"></a>Binden von Timeout Konstanten

Die RPC-Bibliothek verwendet die Bindungs Timeout Konstanten, um die relative Zeitspanne anzugeben, die für das Herstellen einer Bindung an den Server aufgewendet werden soll, bevor ein Timeout auftritt. Das Timeout kann durch einen Aufrufder [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) -Funktion aktiviert werden. In der folgenden Liste sind die gültigen Timeout Werte enthalten.



| Konstante/Wert                                                                                                                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <dt>**RPC \_ C- \_ Bindung \_ unendlich \_ Timeout**</dt> <dt> 10</dt> </dl> | Versucht immer, die Kommunikation immer wiederherzustellen.<br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <dt>**RPC \_ C- \_ Bindung \_ Min. \_ Timeout**</dt> <dt>0</dt> </dl>                   | Versucht, die minimale Zeitspanne für das verwendete Netzwerkprotokoll zu verwenden. Dieser Wert begünstigt die Reaktionszeit gegenüber der Richtigkeit bei der Bestimmung, ob der Server ausgeführt wird.<br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <dt>**RPC \_ C- \_ Bindungs \_ Standard \_ Timeout**</dt> <dt>5</dt> </dl>       | Versucht eine durchschnittliche Zeitspanne für das verwendete Netzwerkprotokoll. Mit diesem Wert wird festgelegt, ob ein Server ausgeführt wird und wie die Antwortzeit Gleichgewicht ist. Dies ist der Standardwert.<br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <dt>**RPC \_ C- \_ Bindung \_ Max. \_ Timeout**</dt> <dt>9</dt> </dl>                   | Versucht den längsten Zeitraum für das verwendete Netzwerkprotokoll. Dieser Wert begünstigt die Richtigkeit bei der Bestimmung, ob ein Server mit der Antwortzeit ausgeführt wird.<br/>                                            |



## <a name="remarks"></a>Bemerkungen

Die Werte in der vorangehenden Tabelle liegen nicht in Sekunden. Diese Werte stellen eine relative Zeitspanne auf einer Skala von 0 bis 10 dar. Weitere Informationen zum Vermeiden von Kommunikations Verzögerungen finden Sie unter verhindern von Client seitigen warte Vorhängen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





