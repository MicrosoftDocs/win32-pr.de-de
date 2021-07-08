---
description: In diesem Artikel wird erläutert, wie Eigenschaftenhandler registriert und verteilt werden, um mit dem Windows zu arbeiten.
ms.assetid: E6E81E04-9CC1-4df5-9A87-DE0CBD177356
title: Registrieren und Verteilen von Eigenschaftenhandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce53f0805c4db5efe38e77ba4e7d1ab5b331c83f
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481925"
---
# <a name="registering-and-distributing-property-handlers"></a>Registrieren und Verteilen von Eigenschaftenhandlern

In diesem Thema wird erläutert, wie Eigenschaftenhandler erstellt und registriert werden, um mit dem Windows zu arbeiten.

Dieses Thema ist wie folgt organisiert:

-   [Registrieren und Verteilen von Eigenschaftenhandlern](#registering-and-distributing-property-handlers)
-   [Überlegungen zur Leistung und Zuverlässigkeit von Eigenschaftenhandlern](#performance-and-reliability-considerations-for-property-handlers)
    -   [Richtlinien für Leistung und Zuverlässigkeit](#guidelines-for-performance-and-reliability)
-   [Verwandte Themen](#related-topics)

## <a name="registering-and-distributing-property-handlers"></a>Registrieren und Verteilen von Eigenschaftenhandlern

Nachdem der Eigenschaftenhandler implementiert wurde, muss er registriert werden, und die Dateierweiterung muss dem Handler zugeordnet werden. Im folgenden Beispiel mit der .recipe-Erweiterung werden die erforderlichen Registrierungseinträge dafür veranschaulicht.

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

Eigenschaftenhandler für einen bestimmten Dateityp werden häufig mit den Anwendungen verteilt, die Dateien dieses Typs erstellen oder bearbeiten. Sie sollten jedoch auch erwägen, Ihre Eigenschaftenhandler unabhängig von diesen Anwendungen zur Verfügung zu stellen, um die Indizierung Ihres Dateityps in Serverszenarien zu unterstützen, in denen Eigenschaftenhandler vom Indexer verwendet werden, die zugehörigen Anwendungen jedoch nicht erforderlich sind. Wenn Sie ein eigenständiges Installationspaket für den Eigenschaftenhandler erstellen, stellen Sie sicher, dass es Folgendes enthält:

-   Die Registrierungsdetails des Eigenschaftenhandlers, die im Thema [Registrieren und Verteilen von Eigenschaftenhandlern angegeben sind.]()
-   Registrierung für Ihren Dateityp und alle Schemadateien, die installiert werden müssen, damit Clients auf alle Funktionen Ihres Eigenschaftenhandlers zugreifen können.

## <a name="performance-and-reliability-considerations-for-property-handlers"></a>Überlegungen zur Leistung und Zuverlässigkeit von Eigenschaftenhandlern

Eigenschaftenhandler werden für jede Datei auf einem bestimmten Computer aufgerufen. Sie werden in der Regel unter den folgenden Umständen aufgerufen:

-   Während der Indizierung der Datei. Dies erfolgt in einem isolierten Prozess mit eingeschränkten Rechten prozess out-of-process.
-   Beim Zugriff auf Dateien im Windows Explorer zum Lesen und Schreiben von Eigenschaftswerten. Dies erfolgt im Prozess.

### <a name="guidelines-for-performance-and-reliability"></a>Richtlinien für Leistung und Zuverlässigkeit

Ein Benutzer kann jederzeit zehntausende Dateien eines bestimmten Typs (einschließlich Ihrer Dateien) auf seinen Computern haben und jederzeit auf diese Dateien zugreifen oder diese ändern. Da Eigenschaftenhandler häufig aufgerufen werden, um diese Zugriffs- und Änderungsvorgänge zu unterstützen, sind die Leistungs- und Zuverlässigkeitsmerkmale Ihres Eigenschaftenhandlers in ausgelasteten, stark parallelen Umgebungen von entscheidender Bedeutung.

Beachten Sie beim Entwickeln und Testen Ihres Eigenschaftenhandlers die folgenden Richtlinien.

-   **Eigenschaftenenumeration**

    Eigenschaftenhandler sollten beim Aufzählen ihrer Eigenschaften eine sehr schnelle Antwortzeit haben. Speicherintensive Berechnungen von Eigenschaftswerten, Netzwerksuchen oder der Suche nach anderen Ressourcen als der Datei selbst sollten vermieden werden, um schnelle Antwortzeiten sicherzustellen.

-   **Schreiben von in-place-Eigenschaften**

    Wenn möglich, sollte beim Umgang mit mittelgroßen oder großen Dateien (mehrere hundert KB oder größer) das Dateiformat so angeordnet werden, dass das Lesen oder Schreiben von Eigenschaftswerten nicht das Lesen der gesamten Datei vom Datenträger erfordert. Selbst wenn die Datei gesucht werden muss, sollte sie nicht vollständig in den Arbeitsspeicher gelesen werden, da dies den Arbeitssatz von Windows Explorer oder dem Windows Search-Indexer überlädt, wenn sie versuchen, auf diese Dateien zu zugreifen oder sie zu indizieren. Weitere Informationen finden Sie unter [Initialisieren von Eigenschaftenhandlern.](./building-property-handlers-property-handlers.md)

    Eine nützliche Methode, um dies zu erreichen, ist das Aufhängen des Headers der Datei mit zusätzlichem Speicherplatz, sodass der Wert beim nächsten Schreiben eines Eigenschaftswerts direkt geschrieben werden kann, ohne dass die gesamte Datei neu geschrieben werden muss. Dies erfordert die ManualSafeSave-Funktionalität. Dieser Ansatz birgt ein gewisses zusätzliches Risiko, dass der Datei-Schreibvorgang unterbrochen wird, während der Schreibvorgang durchgeführt wird (aufgrund eines Systemabsturzes oder Eines Stromausfalls). Da die Eigenschaftengrößen jedoch im Allgemeinen klein sind, ist die Wahrscheinlichkeit einer solchen Unterbrechung ähnlich gering, und die Leistungssteigerungen, die durch das Schreiben von in-place-Eigenschaften erzielt werden können, werden als signifikant genug angesehen, um dieses zusätzliche Risiko zu rechtfertigen. Dennoch sollten Sie ihre Implementierung umfassend testen, um sicherzustellen, dass Ihre Dateien nicht beschädigt sind, falls im Zuge eines Schreibvorgang ein Fehler entsteht.

    Schließlich kann der Vorgang bei der Implementierung von in-place property writing mit ManualSafeSave manchmal nicht vor Ort ausgeführt werden, und der gesamte Stream muss trotzdem umgeschrieben werden. Um das erneute Schreiben zu vereinfachen, unterstützt der während der Handlerin initialisierung bereitgestellte Stream die [**IDestinationStreamFactory-Schnittstelle.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory) Die **IDestinationStreamFactory-Schnittstelle** ermöglicht Handlerimplementierungen, einen temporären Stream zum Schreiben zu erhalten. Wenn alle Schreibvorgänge abgeschlossen sind und die [**IDestinationStreamFactory::GetDestinationStream-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream) aufgerufen wird, wird dieser Stream verwendet, um den ursprünglichen Dateistream vollständig zu ersetzen. Wenn der Zielstream verwendet wird, sollte der ursprüngliche Dateistream als schreibgeschützt behandelt werden, da er durch den Zielstream ersetzt wird, nachdem die **IDestinationStreamFactory::GetDestinationStream-Methode** aufgerufen wurde.

-   **Auswählen ihres COM-Threadingmodells**

    Um die Effizienz Ihres Eigenschaftenhandlers zu maximieren, sollten Sie angeben, dass er das COM-Threadingmodell `Both` verwendet. Dies ermöglicht den direkten Zugriff von STA-Apartment (z. B. Windows Explorer) und Nachrichtenübertragungs-Agent (MTA) (z. B. searchProtocolHost-Prozess in Windows Search), wodurch der Aufwand für das Marshalling in diesen Umgebungen vermieden wird. Um den vollen Nutzen des Threadingmodells zu erzielen, sollten alle Dienste, von denen Ihr Handler abhängt, auch als festgelegt werden, um Marshalling in Aufrufen dieser Komponenten `Both` `Both` zu vermeiden. Überprüfen Sie in der Dokumentation dieser speziellen Dienste, ob sie dieses Threadingmodell verwenden.

-   **Parallelität des Eigenschaftenhandlers**

    Eigenschaftenhandler und die [**IPropertyStore-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertystore) sind für seriellen und nicht für gleichzeitigen Zugriff konzipiert. Windows Explorer, der Windows Search-Indexer und alle anderen Aufrufe von Eigenschaftenhandlern aus Windows Codebasis garantieren diese Verwendung. Es sollte keinen Grund für Dritte geben, einen Eigenschaftenhandler gleichzeitig zu verwenden, aber dieses Verhalten kann nicht garantiert werden. Auch wenn erwartet wird, dass das Aufrufmuster seriell ist, können die Aufrufe auch in verschiedenen Threads erfolgen (z. B. wenn das Objekt remote über COM RPC aufgerufen wird, wie es im Indexer auftritt). Daher müssen Eigenschaftenhandlerimplementierungen das Aufrufen in verschiedenen Threads unterstützen und sollten im Idealfall keine negativen Auswirkungen haben, wenn sie gleichzeitig aufgerufen werden. Da das beabsichtigte Aufrufmuster seriell ist, sollte eine triviale Implementierung mit einem kritischen Abschnitt ausreichen, um diese Anforderungen in den meisten Fällen zu erfüllen. Es ist akzeptabel, das Blockieren gleichzeitiger Aufrufe zu vermeiden, indem Sie die [**TryEnterCriticalSection-Funktion**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) verwenden, um gleichzeitige Aufrufe zu erkennen und zu fehlschlagen.

-   **Datei parallelität**

    Eigenschaftenhandler werden häufig in Szenarien verwendet, in denen mehrere Anwendungen gleichzeitig auf eine Datei zugreifen. Daher müssen der Handler und die Anwendungen die Parallelität verwalten, indem sie beim Öffnen der Datei geeignete Freigabemodi angeben. Sie müssen auch den Zugriff kennen, den die anderen Anwendungen angeben, und um Fälle zu verwalten, in denen der Zugriff nicht zulässig ist. Es ist am besten, wenn alle Verbraucher Gemeinsame Nutzungsmodi angeben, um anderen Benutzern den gleichzeitigen Zugriff auf die Datei zu ermöglichen. Dabei müssen jedoch Konsistenzprobleme verwaltet werden. Entscheidungen zu den am besten geeigneten Freigabemodi müssen im Kontext der Community von Anwendungen getroffen werden, die auf die Datei zugreifen.

    Dateisysteme ermöglichen Es Anwendungen, Dateien so zu öffnen, dass sie steuern können, ob und wie andere Anwendungen die Datei öffnen können. Freigabemodi ermöglichen Lese-, Schreib- und Löschzugriff. Das Eigenschaftensystem unterstützt eine Teilmenge dieser Freigabemodi, wie in der folgenden Tabelle beschrieben.

    

    | Zugriffsmodus                     | Freigabemodus                             |
    |---------------------------------|------------------------------------------|
    | Schreiben                           | Verweigern anderer Leser und Autoren           |
    | Write (EnableShareDenyWrite)    | Aktivieren anderer Leser, Verweigern anderer Writer |
    | Schreibgeschützt (Standard)             | Aktivieren anderer Leser, Verweigern anderer Writer |
    | Schreibgeschützt (EnableShareDenyNone) | Aktivieren anderer Leser und Writer         |

    

     

    Für Schreibzugriff **geöffnete** Eigenschaftenhandler (GPS \_ READWRITE) verweigern anderen Readern und Writern. Handler können ein Verhalten aktivieren, das Lesern ermöglicht, indem sie das Flag in der Registrierung angeben (d. h. `EnableShareDenyWrite` Lesen aktivieren).

    Eigenschaftenhandler, die zum Lesen **geöffnet sind** (GPS DEFAULT), aktivieren standardmäßig andere \_ Reader, verweigern jedoch andere Writer. Handler können andere Writer aktivieren, indem sie das Flag `EnableShareDenyNone` in der Registrierung angeben. Dies bedeutet, dass ein Handler erfolgreich eine Situation behandeln kann, in der sich der Inhalt einer Datei ändert, während der Handler die Datei liest.

    Flagdefinitionen finden Sie unter [**GETPROPERTYSTOREFLAGS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Eigenschaftenhandlern](./building-property-handlers-properties.md)
</dt> <dt>

[Verwenden von Kind-Namen](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Verwenden von Eigenschaftenlisten](./building-property-handlers-property-lists.md)
</dt> <dt>

[Initialisieren von Eigenschaftenhandlern](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Bewährte Methoden und häufig gestellte Fragen zu Eigenschaftenhandlern](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
