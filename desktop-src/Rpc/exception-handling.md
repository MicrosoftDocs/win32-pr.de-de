---
title: Ausnahmebehandlung (RPC)
description: RPC verwendet denselben Ansatz für die Ausnahmebehandlung wie die Windows-API.
ms.assetid: 7133d3f4-ed84-4cde-bc77-88e73ced9073
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25de594a648cddb70f26b42e8b0dbf1d6a9dd51d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474952"
---
# <a name="exception-handling-rpc"></a>Ausnahmebehandlung (RPC)

RPC verwendet denselben Ansatz für die Ausnahmebehandlung wie die Windows-API.

Die [**rpctryschließlich**](rpctryfinally.md)rpcend  /  [](/previous-versions/aa375699(v=vs.80))  /  [**rpcendendlich**](/previous-versions/aa375634(v=vs.80)) -Struktur entspricht der Windows **-Try-End-** Anweisung. Das RPC-Ausnahme-Konstrukt " [**rpctryaußer**](rpctryexcept.md)  /  [**rpcaußer**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)  /  [**rpcendexcept**](/previous-versions/aa375629(v=vs.80)) " entspricht der Windows **-try-** Anweisung.

Wenn Sie die RPC-Ausnahmehandler verwenden, ist der Client seitige Quellcode portabel. Die verschiedenen RPC-Header Dateien, die für jede Plattform bereitgestellt werden, lösen die Makros **rpctry** und [**rpcaußer**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) für jede Plattform auf. In der Windows-Umgebung sind diese Makros direkt den Windows **-try-schließlich** -und **Try-außer-** Anweisungen zugeordnet. In anderen Umgebungen werden diese Makros anderen plattformspezifischen Implementierungen von Ausnahme Handlern zugeordnet.

Mögliche Ausnahmen, die von diesen Strukturen ausgelöst werden, sind der Satz von Fehlercodes, die von den RPC-Funktionen mit den Präfixen RPC \_ S \_ und RPC \_ X und dem Satz der von Windows zurückgegebenen Ausnahmen zurückgegeben werden. Weitere Informationen finden Sie unter [RPC-Rückgabewerte](rpc-return-values.md).

Obwohl die Makros **rpctry** und [**rpcaußer**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) eine anpassbare plattformunabhängige Methode zur Behandlung von Ausnahmen bieten, ist in Windows Vista und höheren Versionen von Windows [**rpcexceptionfilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) die empfohlene Methode zum Behandeln von Ausnahmen. Es ist nicht erforderlich, dass benutzerdefinierte Filter geschrieben werden, um viele der am häufigsten strukturierten Ausnahmen zu erfassen. benutzerdefinierte Ausnahme Filter erfordern jedoch weiterhin **rpcaußer**.

Ausnahmen, die in der Serveranwendung, dem Serverstub und der Server Lauf Zeit Bibliothek (oberhalb der Transportschicht) auftreten, werden an den Client weitergegeben. Es werden keine Ausnahmen von der Server Transport Ebene weitergegeben. Die empfohlene Methode, mit der eine Server Routine Fehler an die RPC-Laufzeit zurückgibt, besteht darin, eine Ausnahme auszulösen. Eine Server Routine kann beliebige Methoden verwenden, die für die Kommunikation von Fehlern zwischen Server Routinen geeignet sind. Wenn jedoch ein Fehler auftritt, der die Ausführung der Remote Prozedur verhindert, sollte eine Ausnahme ausgelöst werden, nachdem die Bereinigung erfolgt ist, und bevor Sie zur RPC-Laufzeit zurückgegeben wird, anstatt einen Wert an RPC zurückzugeben, der nur von der Server Routine als Fehler erkannt wird.

In der folgenden Abbildung wird gezeigt, wie Ausnahmen vom Server an den Client zurückgegeben werden.

![Ausnahmen werden vom Server an den Client über die jeweilige RPC-Laufzeit der einzelnen Komponenten zurückgegeben.](images/prog-a20.png)

Die RPC-Ausnahmehandler unterscheiden sich geringfügig von den of-DCE (Open Software Foundation-Distributed Computing Environment)-Ausnahme Behandlungs Makros **try**, **schließlich** und **catch**. Verschiedene Lieferanten stellen Include-Dateien bereit, die die OSF-DCE-RPC-Funktionen den Microsoft RPC-Funktionen zuordnen, einschließlich **try**, **catch**, **catch** \_ **all** und **EndTry**. Diese Header Dateien ordnen auch die \_ \_ \* Fehlercodes der RPC-Fehlercode-Gegenstücke der OSF-DCE-Ausnahme, RPC \_ S und die Zuordnung \_ \* von RPC x- \_ \_ \* Fehlercodes zu RPC x zu \_ \_ \* . Verwenden Sie für die Portabilität von OSF-DCE diese Includedateien. Weitere Informationen zu den RPC-Ausnahme Handlern finden Sie unter [**rpcexceptionfilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter), [**rpcaußer**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept), [**rpcschließlich**](/previous-versions/aa375699(v=vs.80)). Weitere Informationen zu den Windows-Ausnahme Handlern finden Sie unter [strukturierte Ausnahmebehandlung](/windows/desktop/Debug/structured-exception-handling).

 

 
