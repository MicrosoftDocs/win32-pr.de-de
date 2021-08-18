---
title: Registrieren der Schnittstelle
description: Durch das Registrieren der Schnittstelle, die von einem Serverprogramm unterstützt wird, können Remoteprozeduraufrufe von Clientprogrammen an die richtige Serverroutine gesendet werden.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- Remoteprozeduraufruf RPC , Tasks, Registrieren der Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c444a82d30848f4f01643c08f17f484d027bc7b8c8efe3f10e7f3c194aac26a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926876"
---
# <a name="registering-the-interface"></a>Registrieren der Schnittstelle

Durch das Registrieren der Schnittstelle, die von einem Serverprogramm unterstützt wird, können Remoteprozeduraufrufe von Clientprogrammen an die richtige Serverroutine gesendet werden. Serverprogramme rufen [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) auf, um ihre Schnittstellen zu registrieren. Das folgende Codefragment veranschaulicht seine Verwendung:


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



Der erste Parameter der [**RpcServerRegisterIf-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) ist eine Struktur, die der MIDL-Compiler aus der IDL-Datei generiert, die die Schnittstelle (oder Schnittstellen) für den Server definiert. Der zweite und dritte Parameter sind eine UUID bzw. ein Einstiegspunktvektor. Sie werden in diesem Beispiel auf **NULL** festgelegt. In vielen Fällen legt Ihr Serverprogramm diese Parameterwerte auf **NULL** fest. Serverprogramme verwenden den zweiten und dritten Parameter, wenn sie mehrere Implementierungen derselben Prozeduren in einer Schnittstelle bereitstellen. Weitere Informationen finden Sie unter [Einstiegspunktvektoren.](registering-interfaces.md)

Serverprogramme können auch [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) verwenden, um eine Schnittstelle zu registrieren. Ein Vorteil der Verwendung dieser Funktion besteht darin, dass sie Ihrer Anwendung die Möglichkeit bietet, eine Sicherheitsrückruffunktion festzulegen. Die Verwendung von Sicherheitsrückruffunktionen ist der empfohlene Ansatz zum Sichern einer Schnittstelle.

> [!Note]  
> MIDL erzeugt zwei sehr ähnliche Strukturen: eine für den Client und eine für den Server. Die an die [**RpcServerRegisterIf-Funktion übergebene**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) Struktur ist die Serverversion der von MIDL erzeugten Struktur.

 

 

 




