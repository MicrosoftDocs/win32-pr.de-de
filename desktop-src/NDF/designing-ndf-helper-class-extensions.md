---
title: Entwerfen von NDF-Hilfsklassenerweiterungen
description: Dieses Thema soll allgemeine Anleitungen über den Entwicklungsprozess der Hilfsklassenerweiterung bereitstellen.
ms.assetid: f5dbd198-7d22-4e7e-830e-6753e9f4d6c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 474a9f4ade01fe98a8db30568aa6a7c4978156d2c791747353071f020af27605
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802360"
---
# <a name="designing-ndf-helper-class-extensions"></a>Entwerfen von NDF-Hilfsklassenerweiterungen

Dieses Thema soll allgemeine Anleitungen über den Entwicklungsprozess der Hilfsklassenerweiterung bereitstellen. Die Anleitung in diesem Thema gilt für alle Hilfsklassenerweiterungen. Spezifischere Anleitungen finden Sie unter [Windows Filtering Platform Extensible Helper Class](windows-filtering-platform-extensible-helper-class.md) und [802.11 Wireless Diagnostics Extensible Helper Classes](802-11-wireless-diagnostics-extensible-helper-classes.md).

## <a name="extending-ndf-functionality"></a>Erweitern der NDF-Funktionalität

Windows Vista und höhere Versionen werden mit einer Vielzahl von bereits implementierten Hilfsklassen ausgeliefert, die eine Vielzahl von Problemen diagnostizieren und reparieren können. Manchmal möchten Drittanbieterentwickler diese Hilfsklassen jedoch erweitern, um Spezifische Probleme für ihre jeweiligen Produkte und Implementierungen zu diagnostizieren und zu beheben.

Die folgenden Microsoft NDF-Hilfsklassen sind erweiterbar.

-   [Windows-Filterplattform](windows-filtering-platform-extensible-helper-class.md)
-   [Drahtlose Sicherheit](802-11-wireless-diagnostics-extensible-helper-classes.md)

## <a name="implementing-a-helper-class-extension"></a>Implementieren einer Hilfsklassenerweiterung

Microsoft liefert zwei Schnittstellen, die zum Entwickeln von NDF-Hilfsklassenerweiterungen verwendet werden können.

Die [**INetDiagHelperInfo-Schnittstelle**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) wird von NDF aufgerufen, um zu überprüfen, ob sie über alle erforderlichen Informationen verfügt und die richtige Hilfsklasse ausgewählt hat. Dies erfolgt über die [**GetAttributeInfo-Methode.**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperinfo-getattributeinfo)

Die [**INetDiagHelper-Schnittstelle**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) wird von NDF für die meisten Aktivitäten aufgerufen, die während des Diagnosevorgangs auftreten. Einige seiner Methoden sind erforderlich, andere sind jedoch für bestimmte Verwendungszwecke optional.

Zu den erforderlichen Methoden gehören [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) und [**GetDiagnosticsInfo.**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getdiagnosticsinfo) NDF ruft **Initialize** auf, um Schlüsselparameter an die Hilfsklassenerweiterung zu senden, um ihren Instanzzustand zu initialisieren. **GetDiagnosticsInfo** gibt eine Schätzung an, wie lange die Diagnose dauern kann und ob ein Identitätswechsel des ursprünglichen Benutzerkontexts erforderlich ist.

Eine andere Methode, [**LowHealth,**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth)wird aufgerufen, um die Diagnose für die Netzwerkkomponente durchzuführen, die der Hilfsklasse entspricht. [**Abbrechen**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cancel) wird aufgerufen, wenn NDF feststellt, dass eine laufende Diagnose oder Reparatur beendet werden soll. Die [**Bereinigung**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cleanup) ermöglicht es NDF, NDF-Ressourcen freizugeben, die die Hilfsklassenerweiterung seit dem Aufruf von [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) verwendet hat.

Weitere Informationen zu zusätzlichen Methoden finden Sie unter [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper).

Erweiterungen der NDF-Hilfsklasse werden verwendet, um Konnektivitätsprobleme im Zusammenhang mit einer bestimmten Anwendung oder Komponente zu diagnostizieren und zu beheben. Sie überprüfen auch den Erfolg oder Fehler eines Lösungsversuchs.

Entwickler, die die Implementierung einer Hilfsklassenerweiterung in Betracht ziehen, sollten die folgenden Aufgaben ausführen.

-   Identifizieren Sie Benutzerszenarien, in denen Diagnose- und Reparaturaktionen hilfreich sind.
-   Bereitstellen von Lösungen für häufig auftretende Konnektivitätsprobleme.
-   Wenn eine Hilfsklassenerweiterung erforderlich ist, definieren Sie ein Komponenten-Integritätsmodell, das verwendet wird, um den Integritätszustand der Komponente in NDF darzustellen.

## <a name="identify-user-scenarios"></a>Identifizieren von Benutzerszenarien

Das Testen und Verwenden einer Anwendung hat möglicherweise bereits erkennbare Muster bereitgestellt, die eine Hilfsklassenerweiterung möglicherweise diagnostizieren und reparieren kann. Anwendungsentwickler können diese Daten verwenden, um die wichtigsten Konnektivitätsprobleme zu ermitteln, die behoben werden müssen, und um die Benutzerszenarien zu identifizieren, in denen wahrscheinlich Konnektivitätsprobleme auftreten.

Die Bestimmung der Grundursache der einzelnen Probleme ist in diesem Teil des Prozesses von entscheidender Bedeutung. Dies erfordert möglicherweise umfangreiche Untersuchungen, hilft aber beim Erstellen von Software, die für Benutzer und Administratoren viel einfacher zu verwenden ist. Wenn keine Grundursache identifiziert wird, wird es schwierig oder unmöglich, eine Problembehandlung mithilfe der Hilfsklassenerweiterung anzubieten.

## <a name="provide-resolutions"></a>Bereitstellen von Lösungen

Nachdem ein Entwicklungsteam die Grundursachen von Problemen im Zusammenhang mit seiner Software identifiziert hat, besteht der nächste Schritt darin, die entsprechenden Lösungsaktionen zu identifizieren, die dem Benutzer dabei helfen, das Problem so effizient wie möglich zu lösen.

Nicht alle Lösungen erfordern, dass eine Hilfsklassenerweiterung oder automatisierte Aktion erstellt wird. In einigen Fällen kann das Team feststellen, dass der beste Ansatz zum Auflösen einer Grundursache darin besteht, die Komponente zu beheben oder zu aktualisieren, zusätzliche Hilfeinhalte für die Komponente bereitzustellen oder andere Strategien zu entwickeln, die bessere langfristige Lösungen bieten.

Bei Problemen, bei denen eine automatisierte Aktion ideal ist, ist das Erstellen einer NDF-Hilfsklassenerweiterung häufig eine hervorragende Lösung.

Hilfsklassenerweiterungen geben Informationen zu den Grundursachen und Reparaturinformationen über NDF an Benutzer zurück. Die Zeichenfolgen, die zum Beschreiben der Grundursachen und Reparaturinformationen verwendet werden, müssen für einen nicht technischen Benutzer einfach und leicht verständlich sein. Weitere Informationen zu diesen Zeichenfolgen finden Sie unter [Benutzeroberfläche Guidelines for NDF Helper Class Extensions](user-interface-guidelines-for-ndf-helper-class-extensions.md).

## <a name="define-a-component-health-model"></a>Definieren eines Komponentenzustandsmodells

Softwareentwickler sollten Ebenen der "Integrität" definieren, die mit der Verwaltbarkeit von Netzwerkproblemen verbunden sind. Ein Integritätsmodell, das zum Entwickeln von Hilfsklassen verwendet wird, definiert nur zwei Integritätsebenen: fehlerfrei und fehlerhaft. Diese Ebenen können auch auf NDF-Hilfsklassenerweiterungen angewendet werden.

Eine fehlerfreie Komponente weist auf ein Fehlen von Problemen hin. Eine Komponente kann aufgrund ihrer eigenen Probleme oder aufgrund von Problemen in anderen Komponenten, von denen sie abhängt, als fehlerhaft betrachtet werden.



| Begriff                                                                                                                             | BESCHREIBUNG                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="LowHealth"></span><span id="lowhealth"></span><span id="LOWHEALTH"></span>LowHealth<br/>                         | Dieser Zustand weist auf eine inakzeptable Fehlerstufe dieser Komponente hin, und dass die Komponente das Problem ist.<br/>    |
| <span id="LowHealth_Below"></span><span id="lowhealth_below"></span><span id="LOWHEALTH_BELOW"></span>LowHealth unten<br/> | Dieser Zustand weist auf eine unzulässige Fehlerstufe einer lokalen Computerkomponente hin, von der diese Komponente abhängt.<br/> |



 

Wenn die Diagnose mit NDF durchgeführt wird, wird der Hilfsklassenerweiterung eine Reihe von Fragen gestellt, um ihren Integritätsstatus zu bestimmen. Wenn die Erweiterung antwortet, dass sie fehlerhaft ist, stellt NDF klärende Fragen, versucht, das Problem zu diagnostizieren, seinen Standort und den Nächsten zu suchen. Jede Hilfsklasse muss in der Lage sein, die Frage der niedrigen Integrität zu beantworten, um geeignete Diagnoseaktivitäten besser zu leiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Filtering Platform Extensible Helper Class](windows-filtering-platform-extensible-helper-class.md)
</dt> <dt>

[802.11 Wireless Diagnostics Extensible Helper Classes](802-11-wireless-diagnostics-extensible-helper-classes.md)
</dt> </dl>

 

 





