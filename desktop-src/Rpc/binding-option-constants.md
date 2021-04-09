---
title: Bindungs Options Konstanten (rpcdce. h)
description: Anwendungen legen die Bindungs Options Konstanten fest, um zu steuern, wie Remote Prozedur Aufrufe von der RPC-Lauf Zeit Bibliothek verarbeitet werden. In der folgenden Tabelle sind die einzelnen Bindungseigenschaften und die relevanten Konstanten Werte für die Bindungseigenschaften aufgeführt.
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
ms.openlocfilehash: 52152b5ddcc17abe5c698697e30f1f1a512ee4f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949654"
---
# <a name="binding-option-constants"></a>Bindungs Options Konstanten

Anwendungen legen die Bindungs Options Konstanten fest, um zu steuern, wie Remote Prozedur Aufrufe von der RPC-Lauf Zeit Bibliothek verarbeitet werden. In der folgenden Tabelle sind die einzelnen Bindungseigenschaften und die relevanten Konstanten Werte für die Bindungseigenschaften aufgeführt.

> [!Note]  
> Alle Nachrichten Warteschlangen Optionen (MQ) in der folgenden Tabelle gelten nur für Windows 2000. In Windows XP und höheren Versionen werden Message Queueing nicht unterstützt. Entwickler werden von der Verwendung von Message Queueing abgeraten.

 



| Konstante/Wert                                                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_OPT_BINDING_NONCAUSAL"></span><span id="rpc_c_opt_binding_noncausal"></span><dl> <dt>**RPC \_ C- \_ opt- \_ Bindung, \_ nicht kausal**</dt> <dt>9</dt> </dl>     | Standard. Wenn **false**, eine kausale aufrufsreihen Folge. RPC-Aufrufe werden in strenger Reihenfolge der Übermittlung ausgeführt. Siehe Hinweise.<br/> Wenn **true**, eine nicht kausale aufrufsanordnung. RPC-Aufrufe werden unabhängig ausgeführt. Siehe Hinweise.<br/>                                                                        |
| <span id="RPC_C_OPT_MAX_OPTIONS"></span><span id="rpc_c_opt_max_options"></span><dl> <dt>**RPC \_ C- \_ Option \_ Max. \_ Optionen**</dt> <dt>17</dt> </dl>                      | Für Anwendungsprogramme nicht erforderlich. Wird intern von Microsoft verwendet.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_DONT_FAIL"></span><span id="rpc_c_dont_fail"></span><dl> <dt>**RPC \_ C \_ \_ nicht**</dt> Fehler <dt>4</dt> </dl>                                          | Für Anwendungsprogramme nicht erforderlich. Wird intern von Microsoft verwendet.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_SESSION_ID"></span><span id="rpc_c_opt_session_id"></span><dl> <dt>**RPC \_ C- \_ opt- \_ Sitzungs- \_ ID**</dt> <dt>6</dt> </dl>                          | **True** gibt an, dass für jede Verbindung eine Sitzungs-ID generiert wird.<br/>                                                                                                                                                                                                                                |
| <span id="RPC_C_OPT_COOKIE_AUTH"></span><span id="rpc_c_opt_cookie_auth"></span><dl> <dt>**RPC \_ C- \_ opt- \_ \_ Cookie**</dt> -Authentifizierung <dt>7</dt> </dl>                       | **True** gibt an, dass die Client seitige cookiebasierte Authentifizierung für Verbindungen verwendet wird. Ein Zeiger auf die [**\_ \_ \_ \_ \_ deskriptorstruktur der RPC-C-opt-Cookie**](/windows/desktop/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor) -Authentifizierung wird als *OptionValue* -Parameter in [**rpcbindingsetoption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)übergeben.<br/> |
| <span id="RPC_C_OPT_RESOURCE_TYPE_UUID"></span><span id="rpc_c_opt_resource_type_uuid"></span><dl> <dt>**RPC \_ C- \_ opt- \_ \_ Ressourcentyp \_ UUID**</dt> <dt>8</dt> </dl> | Für Anwendungsprogramme nicht erforderlich. Wird intern von Microsoft verwendet.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_DONT_LINGER"></span><span id="rpc_c_opt_dont_linger"></span><dl> <dt>**RPC \_ C \_ opt \_ dont \_ LINGER**</dt> <dt>13</dt> </dl>                      | Wenn **true**, wird das Herunterfahren der Zuordnung nach dem letzten Bindungs handle/Kontext Handle erzwungen.<br/>                                                                                                                                                                                |
| <span id="RPC_C_OPT_UNIQUE_BINDING"></span><span id="rpc_c_opt_unique_binding"></span><dl> <dt>**RPC \_ C \_ opt \_ Unique \_ Binding**</dt> <dt>11</dt> </dl>             | Wenn der Wert auf **true** festgelegt ist, werden vorhandene Verbindungen von RPC nicht wieder verwendet. Für jede Verbindung wird ein eindeutiges Bindungs Handle geöffnet, und der Status wird für jedes einzelne Bindungs Handle verwaltet.<br/>                                                                                                               |



## <a name="remarks"></a>Bemerkungen

Standardmäßig führt die RPC-Lauf Zeit Bibliothek die Aufrufe für ein angegebenes Bindungs Handle von jedem Thread einer Anwendung in strenger Reihenfolge der Übermittlung aus. Dies garantiert nicht, dass Aufrufe aus unterschiedlichen Threads desselben Bindungs Handles serialisiert werden. Multithreadanwendungen müssen Ihre RPC-Aufrufe serialisieren. Wenn dieses Verhalten zu restriktiv ist, können Sie eine nicht kausale Reihenfolge aktivieren. Wenn Sie dies tun, führt die RPC-Lauf Zeit Bibliothek Aufrufe unabhängig aus. Er erzwingt keine Reihenfolge für die Übermittlung.

Ein Beispiel für eine Anwendung, die möglicherweise eine nicht kausale Reihenfolge nützlich finden kann, ist ein Multithreadprogramm, dessen Threads Aufrufe für dasselbe Bindungs handle ausführen. Entsprechend findet ein Programm, das mehrere asynchrone Aufrufe an einem Bindungs Handle verwendet, eine praktische Option. Ein weiteres Beispiel ist ein Internet Proxy Programm, das einen einzelnen Thread verwendet, um Anforderungen für mehrere Clients zu verarbeiten. In jedem dieser Fälle wäre es äußerst restriktiv, die Remote Prozedur Aufrufe zu serialisieren.

Die Option **RPC \_ C \_ opt \_ dont \_ LINGER** kann nur für Bindungs Handles festgelegt werden, für die die Protokoll Sequenzen **Ncalrpc** oder **ncacn \_ \** _ verwendet werden. Sie kann nicht für _*ncadg \_ \**_ -Protokoll Sequenzen verwendet werden. Die [_ *rpcbindingsetoption* *](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) -Funktion mit dieser Option muss für ein Bindungs Handle aufgerufen werden, für das mindestens ein RPC-Aufruf durchgeführt wurde. Wenn kein RPC-Aufruf für das Bindungs handle erfolgt ist, wird vom **rpcbindingsetoption** -Funktionsaufruf eine **falsche RPC- \_ Art- \_ \_ \_ \_ Bindung** zurückgegeben. Die-Option wird für die gesamte Zuordnung wirksam, unabhängig davon, wie viele Bindungs Handles an die Zuordnung angefügt sind. Da es vor dem zerstören der Zuordnung geprüft wird, kann es zu einem beliebigen Zeitpunkt festgelegt werden, bevor das Bindungs Handle geschlossen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                 |
| Header<br/>                   | <dl> <dt>Rpcdce. h; </dt> <dt>Rpcdcep. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rpcbindingsetoption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**Rpcbindinginqoption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[Verwalten von Netzwerk Verbindungs Sätzen (Zuordnungen)](managing-network-connection-sets-associations-.md)
</dt> </dl>

 

 





