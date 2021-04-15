---
description: Für konfigurierte Komponenten, die in com+-Anwendungen ausgeführt werden, sind Kontexte die Grundlage, auf der com+-Dienste bereitgestellt werden.
ms.assetid: 62a0bef2-c3c2-4a60-a5d1-6c038958e13e
title: Com+-Kontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0ae1228f89797f9124e817db07f11a23dbec12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393181"
---
# <a name="com-contexts"></a>Com+-Kontexte

Für konfigurierte Komponenten, die in com+-Anwendungen ausgeführt werden, sind *Kontexte* die Grundlage, auf der com+-Dienste bereitgestellt werden. In com+ wird ein Kontext als Satz von Lauf Zeiteigenschaften definiert, die einem oder mehreren COM-Objekten zugeordnet sind, die für die Bereitstellung von Diensten für diese Objekte verwendet werden.

In com+ wird jedes COM-Objekt genau einem Kontext zugeordnet, während es ausgeführt wird (d. h. zwischen seiner Aktivierung und Deaktivierung), und jeder Kontext befindet sich in genau einem com-Apartment. Mehrere Objekte können innerhalb desselben Kontexts ausgeführt werden, und mehrere Kontexte können sich im selben Apartment befinden. Wird initialisiert, wenn ein Objekt aktiviert wird. Kontexteigenschaften, wie z. b. Sicherheitskontext Eigenschaften, stellen die Lauf Zeitanforderungen eines Objekts dar.

> [!Note]  
> Für nicht konfigurierte Komponenten, die keine COM+-Dienste verwenden, wird der Kontext größtenteils ignoriert.

 

Com+ verwendet Kontexteigenschaften als Grundlage für die Bereitstellung von Lauf Zeit Diensten. Diese Eigenschaften enthalten den Status, der bestimmt, wie die Ausführungsumgebung Dienste für Objekte innerhalb des Kontexts ausführt. In einigen Fällen können Sie direkt mit den Kontexteigenschaften eines Objekts interagieren, um einen Zustand anzugeben, der für einen Dienst relevant ist, der für das Objekt bereitgestellt wird. Dies wäre z. b. der Fall, wenn ein Objekt, das an einer automatischen Transaktion teilnimmt, das Ergebnis der Transaktion abwählt.

Eine ausführliche Erläuterung der com-Grundlage dieser Konzepte finden Sie unter [Prozesse, Threads und Apartments](/windows/desktop/com/processes--threads--and-apartments).

## <a name="programmatic-interaction-with-context-properties"></a>Programmgesteuerte Interaktion mit Kontexteigenschaften

Jeder Kontext verfügt über ein zugeordnetes [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) -Objekt, mit dem seine Eigenschaften nachverfolgt werden. Sie können auf **ObjectContext** zugreifen, indem Sie die [**GetObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext) -Funktion aufrufen. Nachdem Sie auf **ObjectContext** zugegriffen haben, können Sie Methoden für die [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) -Schnittstelle aufrufen, die Sie zum Bearbeiten von Kontexteigenschaften verfügbar macht.

Wenn Sie z. [**b. IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) aufrufen, wirkt sich das Transaktions Konsistenz Bit auf "konsistent" und die [JIT-Aktivierung](com--just-in-time-activation.md) auf "Done" in dem Kontext aus, der dem Objekt zugeordnet ist. "Konsistent" signalisiert com+, dass für die Transaktion ein Commit ausgeführt wird, und "Done" gibt an, dass das Objekt für die Deaktivierung bereit ist, wenn die Methode zurückgibt.

Zusätzlich zu [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)sind andere spezialisierte Schnittstellen, die Zugriff auf Kontexteigenschaften bereitstellen, [**IObjectContextInfo**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextinfo), [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)und [**IObjectContextActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextactivity). Zu einem bestimmten Block greift [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) auch auf Kontexteigenschaften zu. Sie können [**igetsecuritycallcontext:: getsecuritycallcontext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) zum Abrufen von **ISecurityCallContext** verwenden.

## <a name="understanding-activation-and-interception"></a>Grundlegendes zu Aktivierung und Abfang

Im Allgemeinen müssen Sie den Kontext nur so betrachten, dass er eine Reihe von Eigenschaften darstellt, von denen Sie einige Eigenschaften festlegen oder die Sie für die Bereitstellung von COM+-Diensten für Ihre Komponenten verwenden können. In einigen Fällen müssen Sie jedoch möglicherweise die folgenden beiden miteinander verknüpften Facetten von Kontexten ausführlicher in Erwägung gezogen werden:

-   [Kontext Aktivierung](context-activation.md)oder die Initialisierung eines Objekts in einem geeigneten Kontext.
-   [Abfang](interception-of-cross-context-calls.md)Vorgänge oder Aktionen, die com+ bei Aufrufen über eine Kontext Grenze hinweg durchführt.

## <a name="relation-to-mts-context-wrappers"></a>Beziehung zu MTS-Kontext Wrapper

Kontexte ersetzen die MTS-Kontext Wrapper. Der Zweck der Bereitstellung – das Bereitstellen automatischer Dienste durch das Abfangen von Erstellungs Anforderungen – ist nun eine integrierte Funktion von com+. Folglich ist es nicht mehr erforderlich, die [**saferef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef) -Funktion zu verwenden. In MTS wurde **saferef** verwendet, um einen Verweis auf Ihr Objekt zu erhalten, das außerhalb des Kontext Wrappers übermittelt werden konnte. In com+ ist dies unnötig. normale Objekt Verweise (**diese** Zeiger) funktionieren.

 

 
