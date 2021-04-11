---
description: In diesem Thema wird erläutert, wie Sie Eigenschafts Handler erstellen und registrieren, um mit dem Windows-Eigenschaften System zu arbeiten.
ms.assetid: E6E81E04-9CC1-4df5-9A87-DE0CBD177356
title: Registrieren und Verteilen von Eigenschaften Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1de6af17df8e15912870626935995c67c25f518
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215397"
---
# <a name="registering-and-distributing-property-handlers"></a>Registrieren und Verteilen von Eigenschaften Handlern

In diesem Thema wird erläutert, wie Sie Eigenschafts Handler erstellen und registrieren, um mit dem Windows-Eigenschaften System zu arbeiten.

Dieses Thema ist wie folgt organisiert:

-   [Registrieren und Verteilen von Eigenschaften Handlern](#registering-and-distributing-property-handlers)
-   [Überlegungen zur Leistung und Zuverlässigkeit von Eigenschaften Handlern](#performance-and-reliability-considerations-for-property-handlers)
    -   [Richtlinien für Leistung und Zuverlässigkeit](#guidelines-for-performance-and-reliability)
-   [Zugehörige Themen](#related-topics)

## <a name="registering-and-distributing-property-handlers"></a>Registrieren und Verteilen von Eigenschaften Handlern

Nachdem der Eigenschaften Handler implementiert wurde, muss er registriert werden, und die Dateinamenerweiterung muss dem Handler zugeordnet sein. Im folgenden Beispiel werden die erforderlichen Registrierungseinträge für die Verwendung der. Rezept-Erweiterung veranschaulicht.

```
HKEY_CLASSES_ROOT
   CLSID
      {50d9450f-2a80-4f08-93b9-2eb526477d1a}
         (Default) = Recipe Property Handler
         ManualSafeSave [REG_DWORD] = 00000001
         InProcServer32
            (Default) = C:\\SDK\\PropertyHandlerSample\\bin\\RecipeHandlers.dll
            ThreadingModel = Apartment
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     .recipe
                        (Default) = {50d9450f-2a80-4f08-93b9-2eb526477d1a}
```

Eigenschaften Handler für einen bestimmten Dateityp werden häufig mit den Anwendungen verteilt, die Dateien dieses Typs erstellen oder bearbeiten. Sie sollten jedoch auch in Erwägung gezogen werden, dass Sie die Eigenschaften Handler unabhängig von diesen Anwendungen zur Verfügung stellen, um die Indizierung des Dateityps in Server Szenarios zu unterstützen, in denen Eigenschaften Handler vom Indexer verwendet werden, die zugehörigen Anwendungen jedoch nicht erforderlich sind. Wenn Sie ein eigenständiges Installationspaket für den Eigenschafts Handler erstellen, stellen Sie sicher, dass es Folgendes umfasst:

-   Die Eigenschaften Handler-Registrierungsdetails, die im Thema zum [registrieren und Verteilen von Eigenschaften Handlern]()angegeben sind.
-   Registrierung für Ihren Dateityp und alle Schema Dateien, die installiert werden müssen, damit Clients auf alle Features Ihres Eigenschaften Handlers zugreifen können.

## <a name="performance-and-reliability-considerations-for-property-handlers"></a>Überlegungen zur Leistung und Zuverlässigkeit von Eigenschaften Handlern

Eigenschaften Handler werden für jede Datei auf einem bestimmten Computer aufgerufen. Sie werden in der Regel unter folgenden Umständen aufgerufen:

-   Während der Indizierung der Datei. Dies erfolgt außerhalb des Prozesses in einem isolierten Prozess mit eingeschränkten Rechten.
-   Beim Zugriff auf Dateien in Windows-Explorer, um Eigenschaftswerte zu lesen und zu schreiben. Dies erfolgt in-Process.

### <a name="guidelines-for-performance-and-reliability"></a>Richtlinien für Leistung und Zuverlässigkeit

Ein Benutzer kann jederzeit über Dutzende von Dateien eines beliebigen Typs (einschließlich ihrer) auf seinem Computer verfügen und jederzeit auf eine oder alle dieser Dateien zugreifen oder diese ändern. Da Eigenschafts Handler häufig aufgerufen werden, um diese Zugriffs-und Änderungs Vorgänge zu unterstützen, sind die Leistungs-und Zuverlässigkeits Merkmale Ihres Eigenschafts Handler in ausgelasteten, stark gleichzeitigen Umgebungen von entscheidender Bedeutung.

Beachten Sie beim entwickeln und Testen Ihres Eigenschaften Handlers die folgenden Richtlinien.

-   **Eigenschaftenenumeration**

    Eigenschafts Handler sollten beim Auflisten ihrer Eigenschaften eine sehr schnelle Antwortzeit haben. Speicherintensive Berechnungen von Eigenschafts Werten, netzwerklookups oder der Suche nach anderen Ressourcen als der Datei selbst sollten vermieden werden, um schnelle Reaktionszeiten sicherzustellen.

-   **Schreiben von direkten Eigenschaften**

    Wenn möglich, sollten Sie beim Umgang mit mittelgroßen oder großen Dateien (mehrere hundert KB oder mehr) das Dateiformat so anordnen, dass das Lesen oder Schreiben von Eigenschafts Werten keinen Lesevorgang für die gesamte Datei von der Festplatte erfordert. Auch wenn die Datei gesucht werden muss, sollte Sie nicht vollständig in den Arbeitsspeicher gelesen werden, da Sie das Workingset von Windows Explorer oder den Windows Search-Indexer beim Versuch, auf diese Dateien zuzugreifen oder diese zu indizieren, blobt. Weitere Informationen finden Sie unter [Initialisieren von Eigenschaften Handlern](./building-property-handlers-property-handlers.md).

    Eine sinnvolle Vorgehensweise besteht darin, den Header der Datei mit zusätzlichem Speicherplatz zu auffüllen, damit der Wert beim nächsten Schreiben eines Eigenschafts Werts direkt geschrieben werden kann, ohne die gesamte Datei neu schreiben zu müssen. Hierfür ist die Funktion "manualsafesave" erforderlich. Diese Vorgehensweise birgt ein zusätzliches Risiko, dass der Datei Schreibvorgang unterbrochen werden kann, während der Schreibvorgang ausgeführt wird (aufgrund eines Systemabsturzes oder Stromausfalls), aber da Eigenschafts Größen im Allgemeinen klein sind, ist die Wahrscheinlichkeit einer solchen Unterbrechung ähnlich niedrig, und die Leistungssteigerungen, die durch direktes Schreiben von Eigenschaften erzielt werden können, werden als bedeutend genug angesehen, um dieses zusätzliche Risiko zu Recht Trotzdem sollten Sie darauf achten, dass Sie Ihre Implementierung ausgiebig testen, um sicherzustellen, dass Ihre Dateien nicht beschädigt werden, wenn im Verlauf eines Schreibvorgangs ein Fehler auftritt.

    Beim Implementieren von direkten Schreibvorgängen mit manualsafesave kann der Vorgang manchmal nicht direkt ausgeführt werden, und der gesamte Stream muss auf jeden Fall neu geschrieben werden. Um das erneute Schreiben zu vereinfachen, unterstützt der während der handlerinitialisierung bereitgestellte Stream die [**idestinationstreamfactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory) -Schnittstelle. Die **idestinationstreamfactory** -Schnittstelle ermöglicht Handlerimplementierungen, einen temporären Stream zum Schreiben abzurufen. Wenn alle Schreibvorgänge abgeschlossen sind und die [**idestinationstreamfactory:: getdestinationstream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream) -Methode aufgerufen wird, wird dieser Stream verwendet, um den ursprünglichen Dateistream vollständig zu ersetzen. Wenn der Zielstream verwendet wird, sollte der ursprüngliche Dateistream als schreibgeschützt behandelt werden, da er durch den Zielstream ersetzt wird, nachdem die **idestinationstreamfactory:: getdestinationstream** -Methode aufgerufen wurde.

-   **Auswählen Ihres com-Threading Modells**

    Um die Effizienz des Eigenschaften Handlers zu maximieren, sollten Sie angeben, dass das COM-Threading Modell verwendet werden soll `Both` . Dies ermöglicht den direkten Zugriff auf STA-Apartments (z. b. Windows-Explorer) und MTA (Message Transfer Agent)-Apartments (z. b. den SearchProtocolHost-Prozess in Windows Search), wodurch der Aufwand für das Mars Hallen in diesen Umgebungen vermieden wird. Um den vollen Vorteil des `Both` Threading Modells zu erzielen, sollten alle Dienste, von denen Ihr Handler abhängt, auch als bezeichnet werden, um das Marshalling `Both` bei Aufrufen dieser Komponenten zu vermeiden. Überprüfen Sie die Dokumentation zu diesen speziellen Diensten, um zu überprüfen, ob Sie dieses Threading Modell verwenden.

-   **Eigenschaftenhandlerparallelität**

    Eigenschaften Handler und die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle sind für seriell und nicht für gleichzeitigen Zugriff konzipiert. Windows-Explorer, der Windows Search-Indexer und alle anderen eigenschaftenhandleraufrufe von der Windows-Codebasis garantieren diese Verwendung. Es gibt keinen Grund dafür, dass Dritte einen Eigenschafts Handler gleichzeitig verwenden können, aber dieses Verhalten kann nicht garantiert werden. Auch wenn erwartet wird, dass das aufrufende Muster seriell ist, kann es vorkommen, dass die Aufrufe in verschiedenen Threads erfolgen (z. bWeise, wenn das Objekt remote über com RPC aufgerufen wird, wie im Indexer). Daher müssen eigenschaftenhandlerimplementierungen unterstützen, dass Sie in unterschiedlichen Threads aufgerufen werden, und im Idealfall sollten beim gleichzeitigen aufrufen keine negativen Auswirkungen auftreten. Da das beabsichtigte Aufruf Muster seriell ist, sollte eine triviale Implementierung, die einen kritischen Abschnitt verwendet, ausreichen, um diese Anforderungen in den meisten Fällen zu erfüllen. Es ist zulässig, das Blockieren von gleichzeitigen aufrufen zu vermeiden, indem Sie die [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) -Funktion verwenden, um gleichzeitige Aufrufe zu erkennen und fehlschlagen

-   **Datei Parallelität**

    Eigenschaften Handler werden häufig in Szenarien verwendet, in denen mehrere Anwendungen gleichzeitig auf eine Datei zugreifen. Daher müssen der Handler und die Anwendungen die Parallelität verwalten, indem beim Öffnen der Datei geeignete Freigabe Modi angegeben werden. Außerdem müssen Sie den Zugriff beachten, der von den anderen Anwendungen angegeben wird, sowie Fälle, in denen der Zugriff nicht zulässig ist. Es ist am besten, wenn alle Consumer den freiheitlichen Freigabe Modus angeben, damit andere Benutzer gleichzeitig auf die Datei zugreifen können. dabei müssen jedoch Konsistenzprobleme verwaltet werden. Entscheidungen zu den am besten geeigneten Freigabe Modi, die verwendet werden sollen, müssen im Kontext der Anwendungs Community erfolgen, die auf die Datei zugreifen.

    Dateisysteme ermöglichen Anwendungen das Öffnen von Dateien auf eine Weise, die Ihnen die Kontrolle darüber gibt, ob und wie andere Anwendungen die Datei öffnen können. Freigabe Modi ermöglichen den Zugriff auf Lese-, Schreib-und Löschvorgänge. Das-Eigenschaften System unterstützt eine Teilmenge dieser Freigabe Modi, die in der folgenden Tabelle beschrieben werden.

    

    | Zugriffsmodus                     | Freigabe Modus                             |
    |---------------------------------|------------------------------------------|
    | Schreiben                           | Ablehnen anderer Leser und Writer           |
    | Write (enablesharedenywrite)    | Andere Leser aktivieren, andere Writer ablehnen |
    | Schreibgeschützt (Standard)             | Andere Leser aktivieren, andere Writer ablehnen |
    | Schreibgeschützt (enablesharedenynone) | Andere Reader und Writer aktivieren         |

    

     

    Eigenschaften Handler, die für **Schreib** Vorgänge geöffnet sind (GPS- \_ Lese schreiben), verweigern andere Reader und Writer. Handler können das Verhalten aktivieren, das den Lesern ermöglicht, indem das- `EnableShareDenyWrite` Flag (was das Aktivieren von Read) in der Registrierung angibt.

    Eigenschaften Handler sind zum **Lesen** geöffnet (GPS- \_ Standard), aktivieren standardmäßig andere Leser, verweigern jedoch andere Writer. Handler können andere Writer aktivieren, indem Sie das- `EnableShareDenyNone` Flag in der Registrierung angeben. Dies bedeutet, dass ein Handler eine Situation, in der sich der Inhalt einer Datei ändert, erfolgreich verarbeiten kann, während der Handler die Datei liest.

    Informationen zu flagdefinitionen finden Sie unter [**getpropertystoreflags**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Eigenschaften Handlern](./building-property-handlers-properties.md)
</dt> <dt>

[Verwenden von Kind-Namen](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Verwenden von Eigenschaften Listen](./building-property-handlers-property-lists.md)
</dt> <dt>

[Initialisieren von Eigenschaften Handlern](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Bewährte Methoden und häufig gestellte Fragen zu Eigenschaften Handlern](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
