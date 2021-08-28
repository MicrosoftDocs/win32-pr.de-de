---
title: Marshallingdetails
description: Wenn Sie standardmäßiges Marshalling verwenden, verarbeitet COM alle hier beschriebenen Details für Sie.
ms.assetid: bf3fe212-648e-4d00-ad1d-43d2e5e6a7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f821d06ce452b9492a6b2c5953c5c0d20cd55e653ab471380987dc91566636da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859344"
---
# <a name="marshaling-details"></a>Marshallingdetails

Wenn Sie standardmäßiges Marshalling verwenden, verarbeitet COM alle hier beschriebenen Details für Sie. Es gibt jedoch einige Programmierer, die diese Details und diejenigen benötigen, die an den zugrunde liegenden Informationen interessiert sind. Marshalling ist der Prozess zum Packen und Entpacken von Parametern, damit ein Remoteprozeduraufruf stattfinden kann.

Verschiedene Parametertypen werden auf unterschiedliche Weise gemarshallt. Zum Marshallen eines ganzzahligen Parameters gehört beispielsweise einfach das Kopieren des Werts in den Nachrichtenpuffer. (Obwohl auch in diesem einfachen Fall Probleme wie die Byte reihenfolge bei computerübergreifenden Aufrufen zu behandeln sind.) Das Marshallen eines Arrays ist jedoch ein komplexerer Prozess. Arraymitglieder werden in einer bestimmten Reihenfolge kopiert, damit die andere Seite das Array genau rekonstruieren kann. Wenn ein Zeiger gemarshallt wird, werden die Daten, auf die der Zeigerzeigt, nach den Regeln und Konventionen für den Umgang mit geschachtelten Zeigern in Strukturen kopiert. Es sind eindeutige Funktionen vorhanden, um das Marshalling der einzelnen Parametertypen zu verarbeiten.

Beim standardmäßigen Marshalling sind die Proxys und Stubs systemweite Ressourcen für die Schnittstelle und interagieren über ein Standardprotokoll mit dem Kanal. Standardmäßiges Marshalling kann sowohl von com-definierten Standardschnittstellen als auch von benutzerdefinierten Schnittstellen wie folgt verwendet werden:

-   Bei den meisten COM-Schnittstellen sind die Proxys und Stubs für das standardmäßige Marshalling Prozesskomponentenobjekte, die aus einer systemweiten DLL geladen werden, die von COM in Ole32.dll.
-   Bei benutzerdefinierten Schnittstellen werden die Proxys und Stubs für standardmäßiges Marshalling vom Schnittstellen-Designer generiert, in der Regel mit MIDL. Diese Proxys und Stubs werden statisch in der Registrierung konfiguriert, sodass jeder potenzielle Client die benutzerdefinierte Schnittstelle über Prozessgrenzen hinweg verwenden kann. Diese Proxys und Stubs werden aus einer DLL geladen, die sich über die Systemregistrierung befindet, und verwenden dabei die Schnittstellen-ID (IID) für die benutzerdefinierte Schnittstelle, die sie marshallen.
-   Als Alternative zur Verwendung von MIDL zum Generieren von Proxys und Stubs für benutzerdefinierte Schnittstellen kann stattdessen eine Typbibliothek generiert werden, und das bereitgestellte System, type-libraryâ€"driven marshaling engine, marshallt die Schnittstelle.

Als Alternative zum standardmäßigen Marshalling kann eine Schnittstelle (Standard oder benutzerdefiniert) benutzerdefiniertes Marshalling verwenden. Beim benutzerdefinierten Marshalling implementiert ein Objekt die Proxys zur Laufzeit dynamisch für jede schnittstelle, die es unterstützt. Für jede schnittstelle kann das Objekt com-bereitgestelltes Standard-Marshalling oder benutzerdefiniertes Marshalling auswählen. Diese Auswahl wird vom -Objekt auf Schnittstellenbasis getroffen. Sobald die Auswahl für eine bestimmte Schnittstelle getroffen wurde, bleibt sie während der Lebensdauer des Objekts wirksam. Eine Schnittstelle für ein Objekt kann jedoch benutzerdefiniertes Marshalling verwenden, während eine andere Standard-Marshalling verwendet.

Benutzerdefiniertes Marshalling ist grundsätzlich eindeutig für das Objekt, das es implementiert. Er verwendet Proxys, die vom -Objekt implementiert und zur Laufzeit auf Anforderung für das System bereitgestellt werden. Objekte, die benutzerdefiniertes Marshalling implementieren, müssen die [**IMarshal-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) implementieren, während Objekte, die standardmäßiges Marshalling unterstützen, dies nicht tun.

Wenn Sie eine benutzerdefinierte Schnittstelle schreiben möchten, müssen Sie dafür Marshallingunterstützung bereitstellen. In der Regel stellen Sie eine standardmäßige Marshalling-DLL für die schnittstelle bereit, die Sie entwerfen. Sie können den Proxy-/Stubcode und die Proxy-/Stub-DLL oder eine Typbibliothek erstellen, die COM für das datengesteuerte Marshalling verwendet (mithilfe der Daten in der Typbibliothek).

Damit ein Client eine Schnittstellenmethode in einem Objekt in einem anderen Prozess aufruft, umfasst dies die Zusammenarbeit mehrerer Komponenten. Der Standardproxy ist ein schnittstellenspezifischer Code, der sich im Prozessbereich des Clients befindet und die Schnittstellenparameter für die Übertragung vorbereitet. Sie werden so verpackt oder gemarshallt, dass sie im Empfangsprozess neu erstellt und verstanden werden können. Der Standardstub, ebenfalls ein schnittstellenspezifischer Code, befindet sich im Prozessbereich des Servers und kehrt die Arbeit des Proxys um. Die gesendeten Parameter werden vom Stub entpackt bzw. entmarshaliert und an die Objektanwendung weitergeleitet. Außerdem werden Antwortinformationen verpackt, die an den Client zurück gesendet werden.

> [!Note]  
> Leser, die mit RPC vertrauter sind als COM, können verwendet werden, um die Begriffe Clientstub und Serverstub zu sehen. Diese Begriffe sind analog zu Proxy und Stub.

 

## <a name="components-of-interprocess-communications"></a>Komponenten der prozessübergreifenden Kommunikation

Das folgende Diagramm zeigt den Kommunikationsfluss zwischen den beteiligten Komponenten. Auf der Clientseite der Prozessgrenze durchläuft der Methodenaufruf des Clients den Proxy und dann den Kanal, der Teil der COM-Bibliothek ist. Der Kanal sendet den Puffer mit den gemarshallten Parametern an die RPC-Laufzeitbibliothek, die sie über die Prozessgrenze überträgt. Die RPC-Laufzeit und die COM-Bibliotheken sind auf beiden Seiten des Prozesses vorhanden. Die Unterscheidung zwischen dem Kanal und der RPC-Laufzeit ist ein Merkmal dieser Implementierung und nicht Teil des Programmiermodells oder des konzeptionellen Modells für COM-Client-/Serverobjekte. COM-Server sehen nur den Proxy oder Stub und indirekt den Kanal. Zukünftige Implementierungen verwenden möglicherweise unterschiedliche Ebenen unterhalb des Kanals oder keine Ebenen.

![Diagramm, das die Client.exe und Server.exe auf jeder Seite der Prozessgrenze zeigt.](images/457036c1-98b8-4f35-aebe-70de38112b83.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kanal](channel.md)
</dt> <dt>

[Objektübergreifende Kommunikation](inter-object-communication.md)
</dt> <dt>

[Microsoft RPC](microsoft-rpc.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> <dt>

[Stub](stub.md)
</dt> </dl>

 

 