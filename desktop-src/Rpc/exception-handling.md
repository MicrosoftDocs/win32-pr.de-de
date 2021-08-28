---
title: Ausnahmebehandlung (RPC)
description: RPC verwendet den gleichen Ansatz für die Ausnahmebehandlung wie die Windows-API.
ms.assetid: 7133d3f4-ed84-4cde-bc77-88e73ced9073
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b88cea6e1a2046b957baf5afe72be4cbec9f82d7da32215d2434fbf681f64d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080874"
---
# <a name="exception-handling-rpc"></a>Ausnahmebehandlung (RPC)

RPC verwendet den gleichen Ansatz für die Ausnahmebehandlung wie die Windows-API.

Die [**RpcTryFinally**](rpctryfinally.md)  /  [**RpcFinally**](/previous-versions/aa375699(v=vs.80))  /  [**RpcEndFinally-Struktur**](/previous-versions/aa375634(v=vs.80)) entspricht der Windows **try-finally-Anweisung.** Das RPC-Ausnahmekonstrukt [**RpcTryExcept**](rpctryexcept.md)  /  [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)  /  [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) entspricht der Windows **try-except-Anweisung.**

Wenn Sie die RPC-Ausnahmehandler verwenden, ist ihr clientseitiger Quellcode portierbar. Die verschiedenen RPC-Headerdateien, die für jede Plattform bereitgestellt werden, lösen die **RpcTry-** und [**RpcExcept-Makros**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) für jede Plattform auf. In der Windows-Umgebung werden diese Makros direkt den Windows **try-finally-** und **try-except-Anweisungen** zugeordnet. In anderen Umgebungen werden diese Makros anderen plattformspezifischen Implementierungen von Ausnahmehandlern zugeordnet.

Mögliche Ausnahmen, die von diesen Strukturen ausgelöst werden, umfassen den Satz von Fehlercodes, der von den RPC-Funktionen mit den Präfixen RPC S und RPC X zurückgegeben \_ \_ \_ wird, sowie den Satz von Ausnahmen, die von Windows zurückgegeben werden. Weitere Informationen finden Sie unter [RPC-Rückgabewerte.](rpc-return-values.md)

Während die **RpcTry-** und [**RpcExcept-Makros**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) eine anpassbare plattformunabhängige Methode zum Behandeln von Ausnahmen bieten, ist [**rpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) in Windows Vista und neueren Versionen von Windows die empfohlene Methode zum Behandeln von Ausnahmen. Es müssen keine benutzerdefinierten Filter geschrieben werden, um viele der gängigsten strukturierten Ausnahmen zu erfassen. Benutzerdefinierte Ausnahmefilter erfordern jedoch weiterhin **RpcExcept.**

Ausnahmen, die in der Serveranwendung, dem Serverstub und der Serverlaufzeitbibliothek (über der Transportschicht) auftreten, werden an den Client weitergegeben. Es werden keine Ausnahmen von der Servertransportebene weitergegeben. Die empfohlene Methode für eine Serverroutine zum Zurückgeben von Fehlern an die RPC-Laufzeit ist das Auslösen einer Ausnahme. Eine Serverroutine kann alle Methoden verwenden, die für die Kommunikation von Fehlern zwischen Serverroutinen geeignet sind. Wenn jedoch ein Fehler auftritt, der die Ausführung der Remoteprozedur verhindert, sollte sie nach dem Bereinigen und vor der Rückkehr zur RPC-Laufzeit eine Ausnahme auslösen, anstatt einen Wert an RPC zurückzugeben, der nur von der Serverroutine als Fehler erkannt wird.

Die folgende Abbildung zeigt, wie Ausnahmen vom Server an den Client zurückgegeben werden.

![Ausnahmen werden vom Server über die entsprechende RPC-Laufzeit jeder Komponente an den Client zurückgegeben.](images/prog-a20.png)

Die RPC-Ausnahmehandler unterscheiden sich geringfügig von den Ausnahmebehandlungsmakros OPEN Software Foundation-Distributed Computing Environment (OSF-DCE) **TRY,** **FINALLY** und **CATCH**. Verschiedene Anbieter stellen Dateien bereit, die die RPC-Funktionen OSF-DCE den Microsoft RPC-Funktionen zuordnen, einschließlich **TRY,** **CATCH,** **CATCH** \_ **ALL** und **ENDTRY.** Diese Headerdateien ordnen auch die \_ \_ RPC-S-Fehlercodes \* den OSF-DCE-Ausnahmeentsprechungen, rpc \_ s und RPC \_ \* \_ \_ X-Fehlercodes rpc \* \_ x \_ \* zu. Verwenden Sie diese Includedateien, um DIE OSF-DCE-Portabilität zu nutzen. Weitere Informationen zu den RPC-Ausnahmehandlern finden Sie unter [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter), [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept), [**RpcFinally**](/previous-versions/aa375699(v=vs.80)). Weitere Informationen zu den Windows Ausnahmehandlern finden Sie unter [Strukturierte Ausnahmebehandlung.](/windows/desktop/Debug/structured-exception-handling)

 

 
