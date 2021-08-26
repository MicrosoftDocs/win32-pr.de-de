---
title: Bindungsoptionskonstanten (Rpcdce.h)
description: Anwendungen legen die Bindungsoptionskonstanten fest, um zu steuern, wie die RPC-Laufzeitbibliothek Remoteprozeduraufrufe verarbeitet. In der folgenden Tabelle werden jede Bindungseigenschaft und die relevanten konstanten Werte für die Bindungseigenschaften aufgelistet.
ms.assetid: ff88e05d-b9f3-42ef-a44f-fee9261832c8
topic_type:
- apiref
api_name:
- RPC_C_OPT_BINDING_NONCAUSAL
- RPC_C_OPT_MAX_OPTIONS
- RPC_C_DONT_FAIL
- RPC_C_OPT_SESSION_ID
- RPC_C_OPT_COOKIE_AUTH
- RPC_C_OPT_RESOURCE_TYPE_UUID
- RPC_C_OPT_DONT_LINGER
- RPC_C_OPT_UNIQUE_BINDING
api_location:
- Rpcdce.h
- Rpcdcep.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147d36cf66bb3a45add61b8639ccd3fada31856e72fce8c1f96d7a021e1d5e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023120"
---
# <a name="binding-option-constants"></a>Bindungsoptionskonstanten

Anwendungen legen die Bindungsoptionskonstanten fest, um zu steuern, wie die RPC-Laufzeitbibliothek Remoteprozeduraufrufe verarbeitet. In der folgenden Tabelle werden jede Bindungseigenschaft und die relevanten konstanten Werte für die Bindungseigenschaften aufgelistet.

> [!Note]  
> Alle Nachrichtenwarteschlangenoptionen (MQ) in der folgenden Tabelle sind nur für Windows 2000 gültig. Windows XP und höhere Versionen unterstützen message queuing nicht. Entwicklern wird davon abgeraten, Message Queuing zu verwenden.

 



| Konstante/Wert                                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_OPT_BINDING_NONCAUSAL"></span><span id="rpc_c_opt_binding_noncausal"></span><dl> <dt>**RPC \_ C \_ OPT \_ BINDING \_ NONCAUSAL**</dt> <dt>9</dt> </dl>     | Standard. False gibt an, dass die Reihenfolge kausaler Aufrufe erfolgt. RPC-Aufrufe werden in strenger Reihenfolge der Übermittlung ausgeführt. Siehe Hinweise.<br/> True gibt an, dass die Reihenfolge der nichtcausalen Aufrufe nicht ist. RPC-Aufrufe werden unabhängig ausgeführt. Siehe Hinweise.<br/>                                                                        |
| <span id="RPC_C_OPT_MAX_OPTIONS"></span><span id="rpc_c_opt_max_options"></span><dl> <dt>**RPC \_ C \_ OPT \_ MAX \_ OPTIONS**</dt> <dt>17</dt> </dl>                      | Für Anwendungsprogramme nicht erforderlich. Wird intern von Microsoft verwendet.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_DONT_FAIL"></span><span id="rpc_c_dont_fail"></span><dl> <dt>**RPC \_ C \_ DONT \_ FAIL**</dt> <dt>4</dt> </dl>                                          | Für Anwendungsprogramme nicht erforderlich. Wird intern von Microsoft verwendet.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_SESSION_ID"></span><span id="rpc_c_opt_session_id"></span><dl> <dt>**RPC \_ C \_ OPT \_ SESSION \_ ID**</dt> <dt>6</dt> </dl>                          | True gibt an, dass für jede Verbindung eine Sitzungs-ID generiert wird.<br/>                                                                                                                                                                                                                                |
| <span id="RPC_C_OPT_COOKIE_AUTH"></span><span id="rpc_c_opt_cookie_auth"></span><dl> <dt>**RPC \_ C \_ OPT \_ COOKIE \_ AUTH**</dt> <dt>7</dt> </dl>                       | True gibt an, dass die clientseitige cookiebasierte Authentifizierung für Verbindungen verwendet wird. Ein Zeiger auf die [**RPC C OPT COOKIE \_ \_ \_ \_ AUTH \_ DESCRIPTOR-Struktur**](/windows/desktop/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor) wird als *OptionValue-Parameter* in [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)übergeben.<br/> |
| <span id="RPC_C_OPT_RESOURCE_TYPE_UUID"></span><span id="rpc_c_opt_resource_type_uuid"></span><dl> <dt>**RPC \_ C \_ \_ OPT-RESSOURCENTYP \_ \_ UUID**</dt> <dt>8</dt> </dl> | Für Anwendungsprogramme nicht erforderlich. Wird intern von Microsoft verwendet.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_DONT_LINGER"></span><span id="rpc_c_opt_dont_linger"></span><dl> <dt>**RPC \_ C \_ OPT \_ DONT \_ LINGER**</dt> <dt>13</dt> </dl>                      | True gibt an, dass das Herunterfahren der Zuordnung nach dem Freigeben des letzten Bindungshandle/Kontexthandle für die Zuordnung erzwingen wird.<br/>                                                                                                                                                                                |
| <span id="RPC_C_OPT_UNIQUE_BINDING"></span><span id="rpc_c_opt_unique_binding"></span><dl> <dt>**RPC \_ EINDEUTIGE C \_ \_ \_ OPT-BINDUNG**</dt> <dt>11</dt> </dl>             | Bei Festlegung auf **TRUE** werden vorhandene Verbindungen von RPC nicht wiederverwendet. Für jede Verbindung wird ein eindeutiges Bindungshandle geöffnet, und der Zustand wird für jedes eindeutige Bindungshandle beibehalten.<br/>                                                                                                               |



## <a name="remarks"></a>Hinweise

Standardmäßig führt die RPC-Laufzeitbibliothek die Aufrufe für ein bestimmtes Bindungshandle von jedem Thread einer Anwendung in strenger Reihenfolge der Übermittlung aus. Dies garantiert nicht, dass Aufrufe von verschiedenen Threads auf demselben Bindungshandle serialisiert werden. Multithreadanwendungen müssen ihre RPC-Aufrufe serialisieren. Wenn dieses Verhalten zu restriktiv ist, können Sie die nichtausale Sortierung aktivieren. Wenn Sie dies tun, führt die RPC-Laufzeitbibliothek Aufrufe unabhängig aus. Sie erzwingt keine Reihenfolge bei der Übermittlung.

Ein Beispiel für eine Anwendung, bei der die nichtausale Sortierung nützlich ist, ist ein Multithreadprogramm, dessen Threads Aufrufe für dasselbe Bindungshandle vornehmen. Ebenso findet ein Programm, das mehrere asynchrone Aufrufe für ein Bindungshandle verwendet, eine praktische Option für die nichtausale Sortierung. Ein weiteres Beispiel ist ein Internetproxyprogramm, das einen einzelnen Thread verwendet, um Anforderungen für mehrere Clients zu verarbeiten. In jedem dieser Fälle wäre es äußerst restriktiv, die Remoteprozeduraufrufe zu serialisieren.

Die **OPTION RPC C OPT \_ \_ \_ DONT \_ LINGER** kann nur für Bindungshandles festgelegt werden, die die Protokollsequenzen **ncalrpc** oder **ncacn \_ \** _ verwenden. Sie kann nicht für _*\_ \* ncadg-Protokollsequenzen*_ verwendet werden. Die [*_RpcBindingSetOption-Funktion* *](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) mit dieser Option muss für ein Bindungshandle aufgerufen werden, für das mindestens ein RPC-Aufruf erfolgt ist. Wenn für das Bindungshandle kein RPC-Aufruf erfolgt ist, wird **RPC S WRONG KIND OF \_ \_ \_ \_ \_ BINDING** vom **RpcBindingSetOption-Funktionsaufruf** zurückgegeben. Die Option wird für die gesamte Zuordnung wirksam, unabhängig davon, wie viele Bindungshandles an die Zuordnung angefügt sind. Da sie vor dem Zerstören der Zuordnung überprüft wird, kann sie jederzeit festgelegt werden, bevor das Bindungshandle geschlossen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                 |
| Header<br/>                   | <dl> <dt>Rpcdce.h; </dt> <dt>Rpcdcep.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[Verwalten von Netzwerkverbindungssätzen (Zuordnungen)](managing-network-connection-sets-associations-.md)
</dt> </dl>

 

 





