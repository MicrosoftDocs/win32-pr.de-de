---
title: Registrieren der-Schnittstelle
description: Durch das Registrieren der Schnittstelle, die von einem Serverprogramm unterstützt wird, können Remote Prozedur Aufrufe von Client Programmen an die richtige Server Routine weitergeleitet werden.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Registrieren der Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a12de37b39c719de246ceb79a92d6a51fc361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206234"
---
# <a name="registering-the-interface"></a>Registrieren der-Schnittstelle

Durch das Registrieren der Schnittstelle, die von einem Serverprogramm unterstützt wird, können Remote Prozedur Aufrufe von Client Programmen an die richtige Server Routine weitergeleitet werden. Server Programme aufrufen [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) , um ihre Schnittstellen zu registrieren. Das folgende Code Fragment veranschaulicht seine Verwendung:


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



Der erste Parameter für die [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) -Funktion ist eine Struktur, die der mittlerer l-Compiler aus der IDL-Datei generiert, die die Schnittstelle (bzw. Schnittstellen) für den Server definiert. Der zweite und dritte Parameter sind eine UUID bzw. ein Einstiegspunkt Vektor. Sie werden in diesem Beispiel auf **null** festgelegt. In vielen Fällen werden diese Parameterwerte von Ihrem Serverprogramm auf **null** festgelegt. Server Programme verwenden den zweiten und dritten Parameter, wenn Sie mehrere Implementierungen derselben Prozeduren in einer Schnittstelle bereitstellen. Weitere Informationen finden Sie unter [Einstiegspunkt Vektoren](registering-interfaces.md).

Server Programme können auch [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) zum Registrieren einer Schnittstelle verwenden. Ein Vorteil der Verwendung dieser Funktion besteht darin, dass Sie Ihrer Anwendung die Möglichkeit bietet, eine Sicherheits Rückruffunktion festzulegen. Die Verwendung von Sicherheits Rückruf Funktionen ist die empfohlene Vorgehensweise zum Sichern einer Schnittstelle.

> [!Note]  
> Die Mittel l erzeugt zwei sehr ähnliche Strukturen, eine für den Client und eine für den Server. Die an die Funktion [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) übermittelte Struktur ist die Server Version der von der Mitte erstellten Struktur.

 

 

 




