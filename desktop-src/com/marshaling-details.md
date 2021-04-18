---
title: Marshalling von Details
description: Wenn Sie das standardmäßige Marshalling verwenden, werden alle hier beschriebenen Details von com behandelt.
ms.assetid: bf3fe212-648e-4d00-ad1d-43d2e5e6a7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0fd46ee29c712c6f2b5b286df76a30f1047e6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "106366350"
---
# <a name="marshaling-details"></a>Marshalling von Details

Wenn Sie das standardmäßige Marshalling verwenden, werden alle hier beschriebenen Details von com behandelt. Es gibt jedoch einige Programmierer, die diese Details benötigen, und für diejenigen, die an den zugrunde liegenden Informationen interessiert sind. Beim Marshalling handelt es sich um das Verpacken und entpacken von Parametern, sodass ein Remote Prozedur Aufrufvorgang erfolgen kann.

Unterschiedliche Parametertypen werden auf unterschiedliche Weise gemarshallt. Das Marshalling eines ganzzahligen Parameters umfasst z. b. das einfache Kopieren des Werts in den Nachrichten Puffer. (Obwohl es auch in diesem einfachen Fall Probleme gibt, wie z. b. die Byte-Reihenfolge bei Computer übergreifenden aufrufen.) Das Marshalling eines Arrays ist jedoch komplexer. Arraymember werden in einer bestimmten Reihenfolge kopiert, sodass das Array von der anderen Seite exakt rekonstruiert werden kann. Wenn ein Zeiger gemarshallt wird, werden die Daten, auf die der Zeiger verweist, nach den Regeln und Konventionen für den Umgang mit schsted-Zeigern in Strukturen kopiert. Eindeutige Funktionen sind vorhanden, um das Marshalling der einzelnen Parametertypen zu verarbeiten.

Beim Standardmarshalling sind die Proxys und stubys systemweite Ressourcen für die Schnittstelle, und Sie interagieren mit dem Kanal über ein Standardprotokoll. Standardmäßiges Marshalling kann sowohl durch COM-Standardschnittstellen als auch durch benutzerdefinierte Schnittstellen verwendet werden, wie im folgenden dargestellt:

-   Bei den meisten COM-Schnittstellen sind die Proxys und stubvorgänge für das Standardmarshalling Prozess interne Komponenten Objekte, die aus einer systemweiten dll geladen werden, die von com in Ole32.dll bereitgestellt wird.
-   Im Fall von benutzerdefinierten Schnittstellen werden die Proxys und stufys für das Standard-Marshalling vom Schnittstellen-Designer generiert, in der Regel mit der mittleren l. Diese Proxys und stubys werden statisch in der Registrierung konfiguriert, sodass jeder potenzielle Client die benutzerdefinierte Schnittstelle über Prozess Grenzen hinweg verwenden kann. Diese Proxys und stubys werden mithilfe der Schnittstellen-ID (IID) für die benutzerdefinierte Schnittstelle, die Sie marshallt, aus einer DLL geladen, die sich über die Systemregistrierung befindet.
-   Eine Alternative zur Verwendung von "Mittell" zum Generieren von Proxys und stuften für benutzerdefinierte Schnittstellen kann stattdessen eine Typbibliothek generiert werden, und das vom System bereitgestellte System, das vom System bereitgestellt wird, wird die Schnittstelle Mars Hallen.

Als Alternative zum Standard-Marshalling kann eine Schnittstelle (Standard oder Benutzer definiert) benutzerdefiniertes Marshalling verwenden. Beim benutzerdefinierten Marshalling implementiert ein Objekt die Proxys zur Laufzeit dynamisch für jede Schnittstelle, die es unterstützt. Für eine beliebige Schnittstelle kann das Objekt von com bereitgestelltes Standard Marshalling oder benutzerdefiniertes Marshalling auswählen. Diese Auswahl erfolgt durch das-Objekt auf Schnittstellen Basis. Nachdem die Auswahl für eine bestimmte Schnittstelle getroffen wurde, bleibt Sie während der Lebensdauer des Objekts wirksam. Eine Schnittstelle für ein Objekt kann jedoch ein benutzerdefiniertes Marshalling verwenden, während ein anderes Standardmäßiges Marshalling verwendet.

Das benutzerdefinierte Marshalling ist von Natur aus eindeutig für das Objekt, das es implementiert. Sie verwendet Proxys, die vom-Objekt implementiert werden, und wird für die Anforderung zur Laufzeit dem System bereitgestellt. Objekte, die das benutzerdefinierte Marshalling implementieren, müssen die [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) -Schnittstelle implementieren, wohingegen Objekte, die das Standardmarshalling unterstützen, nicht.

Wenn Sie sich dafür entscheiden, eine benutzerdefinierte Schnittstelle zu schreiben, müssen Sie Marshalling unterstützen. In der Regel stellen Sie eine standardmäßige Marshalling-DLL für die von Ihnen entworfene Schnittstelle bereit. Sie können den Proxy-/Stubcode und die Proxy-/Stub-DLL erstellen, oder Sie können eine Typbibliothek erstellen, mit der com das datengesteuerte Marshalling durchführt (mithilfe der Daten in der Typbibliothek).

Damit ein Client eine Schnittstellen Methode in einem-Objekt in einem anderen Prozess aufruft, umfasst die Zusammenarbeit mehrerer-Komponenten. Der Standard Proxy ist ein Teil Schnittstellen spezifischer Code, der sich im Prozessbereich des Clients befindet und die Schnittstellenparameter für die Übertragung vorbereitet. Sie verpackt oder Marshalls Sie so, dass Sie im Empfangs Prozess neu erstellt und verstanden werden können. Der standardstub, auch ein Teil Schnittstellen spezifischer Code, befindet sich im Prozessbereich des Servers und kehrt die Arbeit des Proxys um. Der Stub entpackt die gesendeten Parameter und leitet Sie an die Objekt Anwendung weiter. Außerdem werden Antwortinformationen verpackt, die an den Client zurückgesendet werden sollen.

> [!Note]  
> Leser, die mit RPC als com vertraut sind, können verwendet werden, um die Begriffe Client-Stub und Server-Stub zu sehen. Diese Begriffe sind analog zu Proxy und Stub.

 

## <a name="components-of-interprocess-communications"></a>Komponenten der prozessübergreifenden Kommunikation

Das folgende Diagramm zeigt den Kommunikationsfluss zwischen den beteiligten Komponenten. Auf der Clientseite der Prozess Grenze durchläuft der Methodenaufrufe des Clients den Proxy und dann auf den Kanal, der Teil der com-Bibliothek ist. Der Kanal sendet den Puffer mit den gemarshallten Parametern an die RPC-Lauf Zeit Bibliothek, die ihn über die Prozess Grenze überträgt. Die RPC-Laufzeit und die com-Bibliotheken sind auf beiden Seiten des Prozesses vorhanden. Der Unterschied zwischen dem Kanal und der RPC-Laufzeit ist ein Merkmal dieser Implementierung und ist nicht Teil des Programmiermodells oder des konzeptionellen Modells für com-Client/Server-Objekte. COM-Server sehen nur den Proxy oder den Stub und, indirekt, den Kanal. In zukünftigen Implementierungen können unter dem Kanal oder ohne Ebenen unterschiedliche Ebenen verwendet werden.

![Diagramm, das die Client.exe-und Server.exe Flows auf jeder Seite mit der Prozess Grenze anzeigt.](images/457036c1-98b8-4f35-aebe-70de38112b83.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kanal](channel.md)
</dt> <dt>

[Kommunikation zwischen Objekten](inter-object-communication.md)
</dt> <dt>

[Microsoft RPC](microsoft-rpc.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> <dt>

[Stub](stub.md)
</dt> </dl>

 

 