---
description: Skalierbarkeit ist die Fähigkeit einer Anwendung, eine zusätzliche Last mit einem linearen Anstieg der Ressourcennutzung zu bedienen.
ms.assetid: 8249f1af-9c96-4545-ad6a-3736c6e63c6d
title: Entwerfen von Skalierbarkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ab0aa9d67afaac14c6d8f59df34183bde36113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344815"
---
# <a name="designing-for-scalability"></a>Entwerfen von Skalierbarkeit

Skalierbarkeit ist die Fähigkeit einer Anwendung, eine zusätzliche Last mit einem linearen Anstieg der Ressourcennutzung zu bedienen. Skalierbarkeit ist in allen verteilten Anwendungen wichtig. Einschränkungen der Skalierbarkeit liegen in der Regel im Zusammenhang mit der Ressourcenverwendung und Abhängigkeiten, die versehentlich im Anwendungs Entwurf erstellt wurden.

In der folgenden Liste werden Skalierbarkeits Probleme beschrieben und Lösungen vorgeschlagen:

-   Ressourcen innerhalb des Computers. Die Anzahl der Threads und der verfügbaren Arbeitsspeicher kann die Skalierbarkeit einschränken. Verwenden Sie ein Threading Modell, das für Ihre Anwendung am effizientesten ist.
-   Computer übergreifende Ressourcen. Die Anzahl der verfügbaren Computer zum Verteilen der Anwendungs Arbeitsauslastung kann die Skalierbarkeit beeinträchtigen.
-   Client Affinität. Zwei Affinitäts Situationen können versehentlich von einer Anwendung erstellt werden: eine Situation, in der die Anwendung vom Zustand aus den Daten abhängt, die der Client mit der Anforderung sendet. und eine Situation, in der die Anwendung einen Client spezifischen Zustand erfordert. Vermeiden Sie das Entwerfen von Zustands Abhängigkeiten zwischen dem Client und der Anwendung.
-   Server Affinität. Eine COM+-Anwendung kann die Skalierbarkeit einschränken, indem Sie eine Server Affinität erstellt, bei der die Anwendung von Informationen zu einem bestimmten Server Computer abhängig ist. Diese Affinität kann bei vielen Daten Bank orientierten Anwendungen auftreten. Die beste Möglichkeit, einen Engpass bei der Server Affinität zu vermeiden, ist das Partitionieren von Daten auf verschiedenen Server Computern. Unterteilen Sie Kundendaten z. b. durch den am häufigsten verwendeten Schlüssel, oder Spannen Sie eine Kundendatenbank über mehrere Server mit dem Nachnamen des Kunden (z. b. Server1: a-f, Server2: g-m, Server3: n-z).
    > [!Note]  
    > Die Daten Partitionierung kann der Programmierlogik eine große Komplexität verleihen und sollte erst ausgeführt werden, nachdem andere Optionen zum Erhöhen der Skalierbarkeit ausprobiert wurden.

     

-   Objekt Lebensdauer. Um skalierbar zu sein, muss eine COM+-Anwendung genau auf die Lebensdauer von Objekten achten. Obwohl ein Objekt vorhanden ist, werden Ressourcen beansprucht. Es ist wichtig, sicherzustellen, dass die Lebensdauer von Objekten, die zu teuren Ressourcen gehören, sorgfältig verwaltet wird. Bei hochleistungsfähigen Objekten, die keine teuren Ressourcen belegen, kann das [com+-Objekt Pooling](com--object-pooling.md) die Skalierbarkeit erhöhen, da Sie die Pooling-Werte administrativ anpassen können, um die Vorteile der Hardware zu nutzen, die Sie möglicherweise haben. Und das ist eine natürliche Möglichkeit zum Steuern von Verbindungen: Wenn Sie z. b. über eine Lizenz für 20 SQL-Verbindungen verfügen, können Sie dies mit der Einstellung "Max Pool" vorschreiben.
-   Gruppieren von Anwendungskomponenten. Um die Skalierbarkeit einer COM+-Anwendung zu verbessern, sollten die Komponenten der mittleren Ebene in zeitabhängige und zeitunabhängige Dienste aufgeteilt werden. Dies ermöglicht es Ihnen, sich auf die Verwendung eines Microsoft Windows-Dienstanbieter zu konzentrieren, um eine erforderliche Komponenten Aktion zu implementieren. Beispielsweise können Sie einen Dienst wie [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) -oder [com+-Komponenten in der Warteschlange](com--queued-components.md) verwenden, um zeitunabhängige, asynchrone Aufgaben zu verarbeiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen für Verfügbarkeit](designing-for-availability.md)
</dt> <dt>

[Entwerfen für die Bereitstellung](designing-for-deployment.md)
</dt> <dt>

[Entwerfen für Sicherheit](designing-for-security.md)
</dt> </dl>

 

 



