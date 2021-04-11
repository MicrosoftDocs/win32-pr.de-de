---
title: Entwerfen von NDF-Hilfsklassen Erweiterungen
description: Dieses Thema soll Ihnen einen generischen Leitfaden über den Entwicklungsprozess der Hilfsklassen Erweiterung bereitstellen.
ms.assetid: f5dbd198-7d22-4e7e-830e-6753e9f4d6c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91ff748d8139aad17fca3710b17e73b5e1eaa14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947593"
---
# <a name="designing-ndf-helper-class-extensions"></a>Entwerfen von NDF-Hilfsklassen Erweiterungen

Dieses Thema soll Ihnen einen generischen Leitfaden über den Entwicklungsprozess der Hilfsklassen Erweiterung bereitstellen. Die Anleitungen in diesem Thema gelten für alle Hilfsklassen Erweiterungen. Genauere Anleitungen finden Sie unter [erweiterbare Hilfsklasse der Windows-Filter Plattform](windows-filtering-platform-extensible-helper-class.md) und [erweiterbare Hilfsklassen für die drahtlose Diagnose von 802,11](802-11-wireless-diagnostics-extensible-helper-classes.md).

## <a name="extending-ndf-functionality"></a>Erweitern der NDF-Funktionalität

Windows Vista und spätere Versionen liefern eine Reihe von bereits implementierten Hilfsklassen, die eine Vielzahl von Problemen diagnostizieren und reparieren können. Manchmal möchten Entwickler von Drittanbietern jedoch möglicherweise diese Hilfsklassen erweitern, um Probleme zu diagnostizieren und zu beheben, die für ihre jeweiligen Produkte und Implementierungen spezifisch sind.

Die folgenden Microsoft NDF-Hilfsklassen sind erweiterbar.

-   [Windows-Filterplattform](windows-filtering-platform-extensible-helper-class.md)
-   [Drahtlose Sicherheit](802-11-wireless-diagnostics-extensible-helper-classes.md)

## <a name="implementing-a-helper-class-extension"></a>Implementieren einer Hilfsklassen Erweiterung

Microsoft verfügt über zwei Schnittstellen, die verwendet werden können, um NDF-Hilfsklassen Erweiterungen zu entwickeln.

Die [**inetdiaghelperinfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) -Schnittstelle wird von NDF aufgerufen, um zu überprüfen, ob Sie über alle erforderlichen Informationen verfügt und die richtige Hilfsklasse ausgewählt hat. Dies wird durch die [**getattributeinfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperinfo-getattributeinfo) -Methode erreicht.

Die [**inetdiaghelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) -Schnittstelle wird von NDF für die meisten Aktivitäten aufgerufen, die während der Diagnose Prozedur auftreten. Einige der Methoden sind erforderlich, andere sind jedoch für bestimmte Verwendungszwecke optional.

Die erforderlichen Methoden sind " [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) " und " [**getdiagnosticsinfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getdiagnosticsinfo)". NDF ruft **initialisieren** auf, um Schlüsselparameter an die Hilfsklassen Erweiterung zu senden, um den Instanzzustand zu initialisieren. **Getdiagnosticsinfo** gibt an, wie lange die Diagnose dauern kann und ob ein Identitätswechsel des ursprünglichen Benutzer Kontexts erforderlich ist.

Eine andere Methode, [**lowhealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), wird aufgerufen, um die Diagnose für die Netzwerkkomponente durchzuführen, die der Hilfsklasse entspricht. [**Abbrechen**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cancel) wird aufgerufen, wenn die NDF eine fortlaufende Diagnose festlegt oder die Reparatur beendet werden soll. Die [**Bereinigung**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cleanup) ermöglicht NDF das Freigeben von NDF-Ressourcen, die von der Hilfsklassen Erweiterung seit dem [**Initialisierungs initialisieren**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) verwendet wurden.

Weitere Informationen zu weiteren Methoden finden Sie unter [**inetdiaghelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper).

NDF-Hilfsklassen Erweiterungen werden verwendet, um Konnektivitätsprobleme zu diagnostizieren und zu beheben, die einer bestimmten Anwendung oder Komponente zugeordnet sind. Außerdem wird überprüft, ob ein Auflösungs Versuch erfolgreich war oder fehlgeschlagen ist.

Entwickler, die die Implementierung einer Hilfsklassen Erweiterung in Erwägung ziehen, sollten die folgenden Aufgaben durchführen.

-   Identifizieren Sie Benutzer Szenarien, in denen Diagnose-und Reparatur Aktionen hilfreich sind.
-   Stellen Sie Lösungen für häufig auftretende Verbindungsprobleme bereit.
-   Wenn eine Hilfsklassen Erweiterung erforderlich ist, definieren Sie ein Komponenten Integritäts Modell, mit dem der Integritäts Status der Komponente in NDF dargestellt wird.

## <a name="identify-user-scenarios"></a>Identifizieren von Benutzer Szenarien

Das Testen und Verwenden einer Anwendung hat möglicherweise bereits diskretierbare Muster bereitgestellt, die eine Hilfsklassen Erweiterung möglicherweise diagnostizieren und möglicherweise reparieren kann. Mit diesen Daten können Anwendungsentwickler die wichtigsten Konnektivitätsprobleme ermitteln und die Benutzer Szenarien ermitteln, in denen Verbindungsprobleme wahrscheinlich auftreten.

In diesem Teil des Prozesses ist es von entscheidender Bedeutung, die Ursache der einzelnen Probleme zu ermitteln. Dies erfordert möglicherweise umfangreiche Recherchen, hilft jedoch bei der Erstellung von Software, die für Benutzer und Administratoren wesentlich einfacher zu verwenden ist. Wenn eine Fehlerursache nicht identifiziert wird, ist es schwierig oder unmöglich, eine Problemlösung mithilfe der Hilfsklassen Erweiterung zu bieten.

## <a name="provide-resolutions"></a>Lösungen bereitstellen

Nachdem ein Entwicklungsteam die Hauptursachen für Probleme identifiziert hat, die mit der Software verbunden sind, besteht der nächste Schritt darin, die entsprechenden Auflösungs Aktionen zu ermitteln, die dem Benutzer helfen, das Problem so effizient wie möglich zu lösen.

Nicht für alle Auflösungen ist es erforderlich, dass eine Hilfsklassen Erweiterung oder eine automatisierte Aktion erstellt wird. In einigen Fällen kann das Team feststellen, dass der beste Ansatz zum Auflösen einer Grundursache darin besteht, die Komponente zu korrigieren oder zu aktualisieren, zusätzlichen Hilfe Inhalt für die Komponente bereitzustellen oder andere Strategien zu entwickeln, die bessere langfristige Lösungen bereitstellen.

Bei Problemen, bei denen eine automatisierte Aktion ideal ist, ist das Erstellen einer NDF-Hilfsklassen Erweiterung häufig eine hervorragende Lösung.

Hilfsklassen Erweiterungen geben Informationen zu Hauptursachen und Reparaturinformationen an Benutzer über NDF zurück. Die Zeichen folgen, die zum Beschreiben der Ursachen und Reparaturinformationen verwendet werden, müssen für einen nichttechnischen Benutzer einfach und leicht verständlich sein. Weitere Informationen zu diesen Zeichen folgen finden Sie unter [Richtlinien für die Benutzeroberfläche für NDF-Hilfsklassen Erweiterungen](user-interface-guidelines-for-ndf-helper-class-extensions.md).

## <a name="define-a-component-health-model"></a>Definieren eines Komponenten Integritäts Modells

Software Entwickler sollten die Ebenen "Health" definieren, die der Verwaltbarkeit von Netzwerkproblemen zugeordnet sind. Ein Integritäts Modell, das zum Entwickeln von Hilfsklassen verwendet wird, definiert nur zwei Integritäts Stufen: fehlerfrei und fehlerhaft. Diese Ebenen können auch auf NDF-Hilfsklassen Erweiterungen angewendet werden.

Eine fehlerfreie Komponente weist auf fehlende Probleme hin. Eine Komponente kann aufgrund ihrer eigenen Probleme als fehlerhaft eingestuft werden, oder aufgrund von Problemen, die in anderen Komponenten auftreten, von denen Sie abhängig ist.



| Begriff                                                                                                                             | BESCHREIBUNG                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="LowHealth"></span><span id="lowhealth"></span><span id="LOWHEALTH"></span>Lowhealth<br/>                         | Dieser Status gibt an, dass diese Komponente nicht akzeptabel ist und dass es sich bei der Komponente um das Problem handelt.<br/>    |
| <span id="LowHealth_Below"></span><span id="lowhealth_below"></span><span id="LOWHEALTH_BELOW"></span>Lowhealth unten<br/> | Dieser Status gibt an, dass eine akzeptable Fehlerstufe von einer lokalen Computerkomponente abhängt, von der diese Komponente abhängt.<br/> |



 

Wenn die Diagnose mithilfe von NDF erfolgt, wird die Erweiterung der Hilfsklasse eine Reihe von Fragen gestellt, um den Zustand der Integrität zu ermitteln. Wenn die Erweiterung antwortet, dass Sie fehlerhaft ist, fordert NDF Fragen zur Problembehebung auf, versucht, das Problem zu diagnostizieren, den Speicherort und den Ort, an dem Sie weiter suchen. Jede Hilfsklasse muss in der Lage sein, die Frage des niedrigen Zustands zu beantworten, um geeignete Diagnose Aktivitäten besser steuern zu können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterbare Hilfsklasse der Windows-Filter Plattform](windows-filtering-platform-extensible-helper-class.md)
</dt> <dt>

[802,11 erweiterbare Hilfsklassen für die drahtlose Diagnose](802-11-wireless-diagnostics-extensible-helper-classes.md)
</dt> </dl>

 

 





