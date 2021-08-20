---
title: Zugriff auf Schnittstellen über Mehrere Schnittstellen hinweg
description: Zugriff auf Schnittstellen über Mehrere Schnittstellen hinweg
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89e82fa29e768328e6c110349627d32e92ab010ce61fdf64141ad3ca7fe9a54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048918"
---
# <a name="accessing-interfaces-across-apartments"></a>Zugriff auf Schnittstellen über Mehrere Schnittstellen hinweg

COM bietet jedem Apartment in einem Prozess die Möglichkeit, Zugriff auf eine Schnittstelle zu erhalten, die für ein Objekt in einem anderen Apartment im Prozess implementiert ist. Dies erfolgt über die [**IGlobalInterfaceTable-Schnittstelle.**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) Diese Schnittstelle verfügt über drei Methoden, die Folgendes ermöglichen:

-   Registrieren einer Schnittstelle als *globale* (prozessweite) Schnittstelle.
-   Erhalten Sie einen Zeiger auf diese Schnittstelle aus einem anderen Apartment über ein Cookie.
-   Widerrufen Sie die globale Registrierung einer Schnittstelle.

Die [**IGlobalInterfaceTable-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) ist eine effiziente Möglichkeit für einen Prozess, einen Schnittstellenzeiger an einem Speicherort zu speichern, auf den von mehreren Ebenen innerhalb des Prozesses zugegriffen werden kann, z. B. prozessweite Variablen und *agile* Objekte (Freithreadobjekte, gemarshallte Objekte), die Schnittstellenzeiger auf andere Objekte enthalten.

Ein agiles Objekt weiß nicht über die zugrunde liegende COM-Infrastruktur, in der es ausgeführt wird. das heißt, in welchem Apartment, Kontext und Thread er ausgeführt wird. Das Objekt kann schnittstellenspezifisch sein, die für ein Apartment oder einen Kontext spezifisch sind. Aus diesem Grund funktioniert das Aufrufen dieser Schnittstellen von überall dort, wo die agile Komponente ausgeführt wird, möglicherweise nicht immer ordnungsgemäß. Die globale Schnittstellentabelle vermeidet dieses Problem, indem sichergestellt wird, dass ein gültiger Proxy (oder direkter Zeiger) auf das Objekt verwendet wird, je nachdem, wo das agile Objekt ausgeführt wird.

> [!Note]  
> Die globale Schnittstellentabelle ist nicht über Prozess- oder Computergrenzen hinweg portierbar und kann daher nicht statt des normalen Mechanismus zur Parameterübergibtung verwendet werden.

 

Informationen zum Erstellen und Verwenden einer globalen Schnittstellentabelle finden Sie in den folgenden Themen:

-   [Erstellen der globalen Schnittstellentabelle](creating-the-global-interface-table.md)
-   [Verwendung der globalen Schnittstellentabelle](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auswählen des Threadingmodells](choosing-the-threading-model.md)
</dt> <dt>

[Multithread-Apartment](multithreaded-apartments.md)
</dt> <dt>

[In-Process-Serverthreadingprobleme](in-process-server-threading-issues.md)
</dt> <dt>

[Prozesse, Threads und Apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Singlethread- und Multithreadkommunikation](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Singlethread-Apartment](single-threaded-apartments.md)
</dt> </dl>

 

 




