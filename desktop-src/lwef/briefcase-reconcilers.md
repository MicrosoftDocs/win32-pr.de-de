---
title: Erstellen von Briefcase-Abstimmungen
description: Ein Abstimmungs-Paar aus Kleinbuchstaben gibt In Kleinbuchstaben die Möglichkeit, verschiedene Versionen eines Dokuments abgleichen.
ms.assetid: 86d66291-96ae-40ea-98ef-ef263f25aa82
keywords:
- Briefcase-Abstimmungen
- Erstattung
- IReconcilableObject
- IReconcileInitiator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4161796999172e6ee9bc7c403e723f9f8bafe7e876b544888fa5e7105b724f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556940"
---
# <a name="creating-briefcase-reconcilers"></a>Erstellen von Briefcase-Abstimmungen

Ein Abstimmungs-Paar aus Kleinbuchstaben gibt In Kleinbuchstaben die Möglichkeit, verschiedene Versionen eines Dokuments abgleichen.

-   [Informationen zu Briefcase-Reconcilern](#about-briefcase-reconcilers)
    -   [Versöhnung](#reconciliation)
    -   [Erstellen eines Briefcase-Reconcilers](#creating-a-briefcase-reconciler)
    -   [Benutzerinteraktion bei der Abstimmung](#user-interaction-in-reconciliation)
    -   [Abgleich eingebetteter Objekte](#reconciling-embedded-objects)
    -   [Rückstände](#residues)
-   [Referenz zur Abstimmung von Kleinbuchstaben](#briefcase-reconciler-reference)
    -   [Schnittstellen und Methoden für die Abstimmung von Kleinbuchstaben](#briefcase-reconciler-interfaces-and-methods)

## <a name="about-briefcase-reconcilers"></a>Informationen zu Briefcase-Reconcilern

Ein Briefcase-Reconciler kombiniert verschiedene Eingabeversionen eines Dokuments, um eine einzelne, neue Ausgabeversion des Dokuments zu erzeugen. Möglicherweise müssen Sie einen Abstimmungstyp für Kleinbuchstaben erstellen, um Ihren Dokumenttyp zu unterstützen. In dieser Übersicht werden Abstimmungen in Kleinbuchstaben beschrieben und erläutert, wie sie erstellt werden.

Die folgenden Themen werden erörtert:

-   [Versöhnung](#reconciliation)
-   [Erstellen eines Briefcase-Reconcilers](#creating-a-briefcase-reconciler)
-   [Benutzerinteraktion bei der Abstimmung](#user-interaction-in-reconciliation)
-   [Abgleich eingebetteter Objekte](#reconciling-embedded-objects)
-   [Rückstände](#residues)

### <a name="reconciliation"></a>Versöhnung

Ein Dokument ist eine Sammlung von Informationen, die kopiert und geändert werden können. Ein Dokument verfügt über unterschiedliche Versionen, wenn der Inhalt von mindestens zwei Kopien des Dokuments unterschiedlich ist. Die Abstimmung erzeugt eine einzelne Version eines Dokuments aus zwei oder mehr Anfangsversionen. In der Regel ist die abgeglichene Version eine Kombination aus Informationen aus den ursprünglichen Versionen mit den neuesten oder nützlichsten Informationen, die beibehalten werden.

Der Abgleich wird durch "Briefcase" initiiert, wenn festgestellt wird, dass zwei oder mehr Kopien desselben Dokuments unterschiedlich sind. In Kleinbuchstaben, die in diesem Kontext als Initiator fungiert, wird der dem angegebenen Dokumenttyp zugeordnete Abstimmungstyp für Kleinbuchstaben gefunden und gestartet. Der Abgleich vergleicht die Dokumente und bestimmt, welche Teile der Dokumente beibehalten werden. Einige Abstimmungen erfordern möglicherweise eine Benutzerinteraktion, um die Abstimmung abschließen zu können. Andere personen können den Abgleich ohne Benutzerinteraktion abschließen. Der Abgleich kann in einer Anwendung enthalten sein oder eine Erweiterung sein, die als DLL implementiert ist.

Einige Abstimmungen in Kleinbuchstaben können zu Einerzungsbeendigten werden. Ein Rückstand ist ein Dokument, das in der Regel den gleichen Dateityp wie das ursprüngliche Dokument auft, das Informationen enthält, die nicht in der zusammengeführten Version gespeichert wurden. In der Regel werden Sie verwendet, um Autoren eine schnelle Möglichkeit zu geben, zu bestimmen, welche Informationen aus ihrem ursprünglichen Dokument nicht in der endgültigen zusammengeführten Version enthalten sind. Wenn ein Abstimmungser einen Bruch unterstützt, erstellt er einen Rückstand für jede der ursprünglichen Versionen des Dokuments. Die Befreiung wird nur erstellt, wenn der Initiator sie an fordert.

Einige Abstimmungen in Kleinbuchstaben arbeiten mit "Briefcase", damit der Benutzer den Abstimmungsabgleich beenden kann. Dies ist ein wichtiges Feature für einen Benutzer, der möglicherweise entscheidet, dass die Abstimmung nicht fortgesetzt werden soll. Ein Abgleich stellt in der Regel ein Beendigungsobjekt zur Unterstützung von Zureigung bei, wenn die Abstimmung eine Benutzerinteraktion erfordert und sehr lang sein kann. In einigen Umgebungen kann ein Abgleich eine Teilabstimmung ermöglichen, sodass ein Benutzer eine Abstimmung vorübergehend ansetzen und später fortsetzen kann. Die Teilabstimmung wird derzeit jedoch nicht von Kleinbuchstaben unterstützt.

### <a name="creating-a-briefcase-reconciler"></a>Erstellen eines Briefcase-Reconcilers

Sie erstellen eine Abstimmung von Kleinbuchstaben, indem Sie die Abstimmungsschnittstellen implementieren. Ein Reconciler implementiert mindestens die [**IReconcilableObject-Schnittstelle**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) und die [IPersistStorage-](/windows/win32/api/objidl/nn-objidl-ipersiststorage) oder [IPersistFile-Schnittstelle.](/windows/win32/api/objidl/nn-objidl-ipersistfile) Als Initiator bestimmt Briefcase, wann eine Abstimmung erforderlich ist, und ruft die [**IReconcilableObject::Reconcile-Methode**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) auf, um die Abstimmung zu initiieren.

Obwohl [**IReconcilableObject::Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) einen umfangreichen Satz von Abstimmungsfunktionen bietet, führt eine Abstimmung von Kleinbuchstaben in den meisten Fällen nur eine minimale Abstimmung aus. Insbesondere erfordert "Briefcase" nicht, dass der Abgleicher die Generierung von Resten oder das Beendigungsobjekt unterstützt. Außerdem führt der Abgleich eine einzelne Von-oben-unten-Abstimmung durch und darf nicht den REC \_ E NOTCOMPLETE-Wert zurückgeben. Das heißt, es sollte nicht versucht werden, einen Teilabgleich \_ zu versuchen.

Der Kleinbuchstaben stellt die [**IReconcileInitiator-Schnittstelle**](ireconcileinitiator.md) bereit. Der Briefcase-Abgleicher kann die [**IReconcileInitiator::SetAbortCallback-Methode**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback) verwenden, um das Beendigungsobjekt fest zu legen. In Großbuchstaben werden keine Versionsbezeichner verwendet, und daher können keine früheren Versionen eines Dokuments angegeben werden, wenn sie von einem Abgleicher mithilfe der entsprechenden Methoden in **IReconcileInitiator abgeslangt werden.**

Die Großbuchstaben werden an [**IReconcilableObject::Reconcile-Dateimoniker**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) übergibt, die die Versionen des zu abstimmenden Dokuments darstellen. Die Abstimmung von Kleinbuchstaben erhält zugriff auf die Versionen mithilfe der [IMoniker::BindToObject-](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) oder [IMoniker::BindToStorage-Methode.](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) Letzteres ist im Allgemeinen schneller und wird empfohlen. Der Abgleicher muss alle Objekte oder Speicher frei geben, an die er gebunden ist.

Wenn die Abstimmung von Kleinbuchstaben [IMoniker::BindToStorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage)verwendet, wird sie an einen Speicher gebunden, der entweder flacher Speicher (ein Stream) oder OLE-definierter strukturierter Speicher ist. Wenn der Abgleicher flachen Speicher erwartet, sollte er IMoniker::BindToStorage verwenden, um die [IStream-Schnittstelle an](/windows/win32/api/objidl/nn-objidl-istream) fordern. Wenn die Abstimmung strukturierten Speicher erwartet, sollte sie die [IStorage-Schnittstelle](/windows/win32/api/objidl/nn-objidl-istorage) anfordern. In beiden Fällen sollte er schreibgeschützten direkten (nicht übersetzten) Zugriff auf den Speicher anfordern. Lese-/Schreibzugriff ist möglicherweise nicht verfügbar.

Eine minimale Abstimmung von Kleinbuchstaben untersucht in der Regel direkt den Speicher der anderen Versionen und behandelt eingebettete Objekte sehr primitiv, z. B. durch Zusammenführen von zwei Versionen des Objekts, indem beide Versionen in die Ausgabeversion eingebunden werden.

Der Initiator sucht mithilfe einer Teilmenge der Logik, die von der [GetClassFile-Funktion](/windows/win32/api/objbase/nf-objbase-getclassfile) implementiert wird, den Typ einer bestimmten Datei und sucht dann in der Registrierung nach der Abstimmungsklasse, die dem angegebenen Dateityp zugeordnet ist. Der Typ einer Datei wird wie bei anderen Shell-Komponenten nur durch die Dateierweiterung bestimmt. Die Erweiterung einer Datei muss einen registrierten Dateityp für "Briefcase" haben, um einen Abstimmungsserver für die Datei aufrufen zu können. Sie müssen einen Registrierungseintrag im folgenden Formular festlegen, wenn Sie die Abstimmung installieren.

```
CLSID
   {the file CLSID}
      Roles
         Reconciler
            (Default) = {the reconciler-classid}
```

Die -Klasse muss schnell geladen werden, muss als MULTIPLEUSE festgelegt sein und muss, sofern keine Marshaller für die Abstimmungsschnittstelle bereitgestellt werden, ein Prozessserver (in einer DLL enthalten) und nicht ein lokaler Server (implementiert in einer \_ .exe-Datei) sein.

### <a name="user-interaction-in-reconciliation"></a>Benutzerinteraktion bei der Abstimmung

Eine Abstimmung mit Kleinbuchstaben sollte versuchen, eine Abstimmung ohne Benutzerinteraktion durchführen. Desto automatisierter die Abstimmung, desto besser wird die Wahrnehmung des Prozesses durch den Benutzer.

In einigen Fällen kann der Benutzereingriff nützlich sein. Ein Dokumentsystem kann z. B. verlangen, dass ein Benutzer Änderungen überprüft, bevor er die zusammengeführte Version eines Dokuments akzeptiert, oder er benötigt Kommentare vom Benutzer, die die vorgenommenen Änderungen erläutern. In diesen Fällen ist der Initiator und nicht der Briefkoffer für die Abfrage des Benutzers und die Ausführung der Anweisungen des Benutzers verantwortlich.

In anderen Fällen kann ein Benutzereingriff erforderlich sein, z. B. wenn zwei Versionen auf inkompatible Weise bearbeitet wurden. In solchen Fällen muss entweder der Initiator oder die Briefcase-Abstimmung den Benutzer abfragen, um Anweisungen zum Lösen des Konflikts zu erhalten. Im Allgemeinen kann sich kein Initiator darauf verlassen, dass eine Abstimmung abgeschlossen wird, ohne dass eine Benutzerinteraktion erwartet wird. Abstimmungen haben hingegen die Möglichkeit, mit dem Benutzer zu interagieren, um Konflikte aufzulösen oder dies vom Initiator zu verlangen.

### <a name="reconciling-embedded-objects"></a>Abgleich eingebetteter Objekte

Wenn ein Dokument abgeglichen wird, kann der Briefcase-Abgleich selbst zum Initiator werden, wenn er ein eingebettetes Objekt eines Typs entdeckt, der nicht abgeglichen werden kann. In diesem Fall muss die Abstimmung jedes eingebettete Objekt rekursiv abstimmen und alle Aufgaben eines Initiators übernehmen.

Um die Rekursion durchführen zu können, lädt die Briefcase-Abstimmung das Objekt und fragt die entsprechende Schnittstelle ab. Der Handler für das -Objekt muss die -Schnittstelle unterstützen. Wenn eine Methode der -Schnittstelle den OLE \_ E NOTRUNNING-Wert zurückgibt, muss der Abgleicher das -Objekt ausführen, um \_ den Vorgang ausführen zu können. Da Code für eingebettete Objekte nicht immer verfügbar ist, muss eine Abstimmung eine Lösung für diese Bedingung bereitstellen. Beispielsweise kann die Abstimmung sowohl alte als auch neue Versionen des eingebetteten Objekts in der abgestimmten Version enthalten. Der Abgleicher darf nicht versuchen, linksübergreifend eine Abstimmung zu versuchen.

Der Initiator speichert die zusammengeführten Dokumentversionen. In vielen Fällen hat der Initiator Zugriff auf den Speicher jeder Version und speichert das Ergebnis der Abstimmung mithilfe eines ähnlichen Speichers. Manchmal kann der Initiator jedoch über ein In-Memory-Objekt verfügen, für das keine persistente Version verfügbar ist. Diese Situation kann auftreten, wenn ein Dokument, das geöffnete eingebettete Objekte enthält, vor dem Speichern abgestimmt werden muss. In solchen Fällen speichert der Initiator das Ergebnis der Abstimmung in der Im Arbeitsspeicher gefundenen Version.

Der Initiator verwendet die [IPersistStorage-Schnittstelle,](/windows/win32/api/objidl/nn-objidl-ipersiststorage) um die zusammengeführte Version zu binden (zu laden). Der Initiator verwendet die [IPersistStorage::Load-Methode,](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) wenn bereits eine erste Version erstellt wurde, und verwendet die [IPersistStorage::InitNew-Methode](/windows/win32/api/objidl/nf-objidl-ipersiststorage-initnew) für die erste Version. Wenn die zusammengeführte Version geladen wird, verwendet der Initiator [QueryInterface,](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) um die Adresse der [**IReconcilableObject-Schnittstelle**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) abzurufen. Diese Schnittstelle ermöglicht dem Initiator den Zugriff auf die Speicherung der vorhandenen 1000-000-Daten und ermöglicht die Erstellung von Speicher für neue Ingen. Anschließend leitet der Initiator die Schnittstelle an, um die Abstimmung durchführen zu können. Der Initiator fragt tatsächlich die [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile) vor IPersistStorage ab. Wenn der Reconciler IPersistFile unterstützt, bearbeitet der Initiator das Replikat über die IPersistFile anstelle der IPersistStorage-Methoden. Dies ermöglicht den Abgleich von Dateien, die nicht als Verbunddokumente gespeichert sind.

Nach Abschluss der Abstimmung kann der Initiator die zusammengeführte Version mithilfe der [IPersistStorage-](/windows/win32/api/objidl/nn-objidl-ipersiststorage) oder [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile) speichern. Während des Abgleichs erstellt der Abstimmungs-Abgleich von Kleinbuchstaben bei Bedarf eine Belagerung und schreibt ihre persistenten Bits in den Speicher. Wenn die zusammengeführte Version ein Stream ist, enthält die an [IPersistStorage::Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) übergebene [IStorage-Schnittstelle](/windows/win32/api/objidl/nn-objidl-istorage) einen Stream namens "Contents", dessen Speicherstatus auf STATEBITS FLAT festgelegt \_ ist. (Sie können die Zustandsbits mithilfe der [IStorage::Stat-Methode](/windows/win32/api/objidl/nf-objidl-istorage-stat) festlegen.) Nach der Zusammenführung speichert der Initiator die zusammengeführte Version, indem er die Daten entsprechend schreibt. Es sollte sichergestellt werden, dass STATEBITS \_ FLAT für den Speicher entsprechend festgelegt ist.

### <a name="residues"></a>Rückstände

Der Initiator gibt an, ob er beim Aufrufen der [**IReconcilableObject::Reconcile-Methode**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) den *Parameter pstgNewResidues* auf eine gültige Adresse festlegen möchte. Wenn der Abgleicher die Erstellung von Stichen nicht unterstützt, muss er sofort den REC E NORESIDUES-Wert zurückgeben, es sei denn, der dwFlags-Parameter gibt den \_ \_ **RECONCILEF \_ NORESIDUESOK-Wert** an. 

Der Abstimmungsator für Kleinbuchstaben gibt dem Initiator einen Fehler zurück, indem er neue Speicherelemente erstellt und in das Array kopiert, auf das *pstgNewResidues zeigt.* Bei strukturierten Speicherbenutzeroberflächen kopiert der Abgleicher eine [IStorage-Schnittstelle,](/windows/win32/api/objidl/nn-objidl-istorage) und für Flat Storage-Ausfälle wird entweder eine [IStream-](/windows/win32/api/objidl/nn-objidl-istream) oder eine IStorage-Schnittstelle kopiert, für die das FLAG STATEBITS FLAT festgelegt \_ ist. Der Abgleicher verwendet IStorage, um den erforderlichen Speicher zu erstellen, indem er [IStorage::CreateStream](/windows/win32/api/objidl/nf-objidl-istorage-createstream) verwendet, um flachen Speicher für einen Rest zu erstellen, bei dem es sich um einen Stream handelt, und [IStorage::CreateStorage,](/windows/win32/api/objidl/nf-objidl-istorage-createstorage) um strukturierten Speicher zu erstellen.

Der Initiator bereitet *pstgNewResidues* so vor, dass er keine Elemente im nicht reservierten Teil des [IStorage-Namespace](/windows/win32/api/objidl/nn-objidl-istorage) enthält. Die Abstimmung von Kleinbuchstaben platziert jeden Rest in einem Element, dessen Name der Reihenfolge seiner ursprünglichen Version entspricht. Beispielsweise ist der erste Rest in "1", der zweite in "2" und so weiter enthalten. Wenn das abgeglichene Objekt selbst einen Rückstand erzeugt, befindet es sich im Element mit dem Namen "0".

Der Abstimmungsator für Kleinbuchstaben committ jedes neu erstellte Element einzeln und stellt sicher, dass der Initiator Zugriff auf die Informationen hat. Der Reconciler führt jedoch keinen Commit *für pstgNewResidues selbst* aus. Der Initiator ist dafür verantwortlich, dies zu committen oder anderweitig zu verdringen.

## <a name="briefcase-reconciler-reference"></a>Referenz zur Abstimmung von Kleinbuchstaben

Dieser Abschnitt enthält Informationen zu den Abstimmungsschnittstellen. Bei der Behandlung von Fehlern kann eine Methode nur die Fehlerwerte zurückgeben, die explizit als mögliche Rückgabewerte definiert sind. Darüber hinaus muss die -Methode alle Variablen, deren Adressen als Parameter übergeben werden, auf **NULL** festlegen, bevor der Fehler zurückgegeben wird.

### <a name="briefcase-reconciler-interfaces-and-methods"></a>Schnittstellen und Methoden für die Abstimmung von Kleinbuchstaben

-   [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) 
    -   -   [**IReconcilableObject::GetProgressFeedbackMaxEstimate**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-getprogressfeedbackmaxestimate)
        -   [**IReconcilableObject::Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile)

-   [**IReconcileInitiator**](ireconcileinitiator.md) 
    -   -   [**IReconcileInitiator::SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)
        -   [**IReconcileInitiator::SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback)

-   [**INotifyReplica**](/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica) 
    -   -   [**INotifyReplica::YouAreAReplica**](/windows/desktop/api/reconcil/nf-reconcil-inotifyreplica-youareareplica)

 

 