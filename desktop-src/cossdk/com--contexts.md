---
description: Für konfigurierte Komponenten, die in COM+-Anwendungen ausgeführt werden, sind Kontexte die Grundlage, auf der COM+-Dienste bereitgestellt werden.
ms.assetid: 62a0bef2-c3c2-4a60-a5d1-6c038958e13e
title: COM+-Kontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c48e2fb9a118bff5fe4d6590ff859f0f053ab29687d4f4a2a070d44af37b25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730650"
---
# <a name="com-contexts"></a>COM+-Kontexte

Für konfigurierte Komponenten, die in COM+-Anwendungen ausgeführt werden, sind *Kontexte* die Grundlage, auf der COM+-Dienste bereitgestellt werden. In COM+ wird ein Kontext als Satz von Laufzeiteigenschaften definiert, die einem oder mehrere COM-Objekten zugeordnet sind, die zum Bereitstellen von Diensten für diese Objekte verwendet werden.

In COM+ wird jedem COM-Objekt genau ein Kontext zugeordnet, während es ausgeführt wird (d. h. zwischen seiner Aktivierung und Deaktivierung), und jeder Kontext befindet sich genau in einem COM-Apartment. Mehrere Objekte können innerhalb desselben Kontexts ausgeführt werden, und mehrere Kontexte können sich innerhalb desselben Apartment befinden. Wenn ein Objekt aktiviert wird, stellen Kontexteigenschaften, z. B. Sicherheitskontexteigenschaften, die Laufzeitanforderungen eines Objekts dar.

> [!Note]  
> Bei nicht konfigurierten Komponenten, die keine COM+-Dienste verwenden, wird der Kontext größten teils ignoriert.

 

COM+ verwendet Kontexteigenschaften als Grundlage für die Bereitstellung von Laufzeitdiensten. Diese Eigenschaften enthalten einen Zustand, der bestimmt, wie die Ausführungsumgebung Dienste für Objekte innerhalb des Kontexts ausführt. In einigen Fällen können Sie direkt mit den Kontexteigenschaften eines Objekts interagieren, um einen Zustand anzugeben, der für einen Dienst relevant ist, der für das Objekt bereitgestellt wird. Dies würden Sie beispielsweise tun, wenn ein Objekt, das an einer automatischen Transaktion beteiligt ist, über das Ergebnis der Transaktion abstimmet.

Eine ausführliche Erläuterung der COM-Grundlage dieser Konzepte finden Sie unter [Prozesse, Threads und Apartment](/windows/desktop/com/processes--threads--and-apartments).

## <a name="programmatic-interaction-with-context-properties"></a>Programmgesteuerte Interaktion mit Kontexteigenschaften

Jedem Kontext ist ein [**ObjectContext-Objekt zugeordnet,**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) das seine Eigenschaften nachverfolgt. Sie können auf **ObjectContext zugreifen,** indem Sie die [**GetObjectContext-Funktion**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext) aufrufen. Nachdem Sie auf **ObjectContext** zugegriffen haben, können Sie Methoden für die [**IObjectContext-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) aufrufen, die verfügbar macht, um Kontexteigenschaften zu bearbeiten.

Beispielsweise hat der Aufruf von [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) den Effekt, dass das Transaktionskonsistenzbit auf "consistent" und die [JIT-Aktivierungs-Done-Bit](com--just-in-time-activation.md) auf "done" im Kontext festgelegt wird, der dem -Objekt zugeordnet ist. "Konsistent" signalisiert COM+, dass Sie für den Commit der Transaktion abstimmen, und "done" gibt an, dass Ihr Objekt deaktiviert werden kann, wenn die Methode zurückgegeben wird.

Zusätzlich zu [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)sind [**IObjectContextInfo,**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextinfo) [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)und [**IObjectContextActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextactivity)weitere spezialisierte Schnittstellen, die Zugriff auf Kontexteigenschaften bieten. In einem bestimmten Umfang greifen [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) auch auf Kontexteigenschaften zu. Sie können [**IGetSecurityCallContext::GetSecurityCallContext verwenden,**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) um **ISecurityCallContext zu erhalten.**

## <a name="understanding-activation-and-interception"></a>Grundlegendes zu Aktivierung und Abfangen

Im Allgemeinen müssen Sie den Kontext nur in dem Umfang betrachten, in dem er eine Reihe von Eigenschaften darstellt, von denen sie einige festlegen oder erhalten können, die zum Bereitstellen von COM+-Diensten für Ihre Komponenten verwendet werden. In einigen Fällen müssen Sie jedoch möglicherweise die folgenden zwei miteinander verknüpften Facets von Kontexten ausführlicher betrachten:

-   [Kontextaktivierung](context-activation.md)oder die Initialisierung eines Objekts in einem geeigneten Kontext.
-   [Abfangen](interception-of-cross-context-calls.md)von , oder was COM+ bei Aufrufen über eine Kontextgrenze hinweg tut.

## <a name="relation-to-mts-context-wrappers"></a>Beziehung zu MTS-Kontext-Wrappern

Kontexte ersetzen effektiv die MTS-Kontext-Wrapper. Der Zweck, den sie erfüllt haben – das Bereitstellen automatischer Dienste durch das Auffangen von Erstellungsanforderungen – ist jetzt ein integriertes Feature von COM+. Daher müssen Sie die [**SafeRef-Funktion nicht mehr**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef) verwenden. In MTS wurde **SafeRef** verwendet, um einen Verweis auf Ihr Objekt zu erhalten, der außerhalb des Kontext-Wrappers übergeben werden konnte. In COM+ ist dies nicht erforderlich. normale Objektverweise **(diese** Zeiger) funktionieren.

 

 
