---
title: Erstellen von Briefcase-abgleichen
description: 'Eine Aktentasche-Abstimmung ermöglicht Brief: die Möglichkeit, unterschiedliche Versionen eines Dokuments abzugleichen.'
ms.assetid: 86d66291-96ae-40ea-98ef-ef263f25aa82
keywords:
- Brief Synchronisierer
- Erstattung
- Ireconcilableobject
- Ireconcileinitiator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b925e7055e15f6c7a49408aa28d147fb2eef5a7e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390160"
---
# <a name="creating-briefcase-reconcilers"></a>Erstellen von Briefcase-abgleichen

Eine Aktentasche-Abstimmung ermöglicht Brief: die Möglichkeit, unterschiedliche Versionen eines Dokuments abzugleichen.

-   [Informationen über die Abgleichen von Brief Fällen](#about-briefcase-reconcilers)
    -   [Ö](#reconciliation)
    -   [Erstellen eines Briefcase-abversers](#creating-a-briefcase-reconciler)
    -   [Benutzerinteraktion bei Abstimmung](#user-interaction-in-reconciliation)
    -   [Abgleichen von eingebetteten Objekten](#reconciling-embedded-objects)
    -   [Stoff](#residues)
-   [Referenz zur Briefcase-Synchronisierung](#briefcase-reconciler-reference)
    -   [Schnittstellen und Methoden der Briefcase-Synchronisierung](#briefcase-reconciler-interfaces-and-methods)

## <a name="about-briefcase-reconcilers"></a>Informationen über die Abgleichen von Brief Fällen

Eine Aktentasche-Synchronisierung kombiniert verschiedene Eingabe Versionen eines Dokuments, um eine einzelne, neue Ausgabe Version des Dokuments zu generieren. Möglicherweise müssen Sie eine Aktentasche-Konfiguration erstellen, um Ihren Dokumenttyp zu unterstützen. In dieser Übersicht werden die Protokolle von Brief Fällen beschrieben und erläutert, wie Sie erstellt werden.

Die folgenden Themen werden erörtert:

-   [Ö](#reconciliation)
-   [Erstellen eines Briefcase-abversers](#creating-a-briefcase-reconciler)
-   [Benutzerinteraktion bei Abstimmung](#user-interaction-in-reconciliation)
-   [Abgleichen von eingebetteten Objekten](#reconciling-embedded-objects)
-   [Stoff](#residues)

### <a name="reconciliation"></a>Ö

Ein Dokument ist eine Sammlung von Informationen, die kopiert und geändert werden können. Ein Dokument weist verschiedene Versionen auf, wenn sich der Inhalt mindestens zweier Kopien des Dokuments unterscheidet. Die Abstimmung erzeugt eine einzelne Version eines Dokuments aus mindestens zwei Versionen. In der Regel ist die abgestimmte Version eine Kombination aus Informationen aus den anfänglichen Versionen mit den neuesten oder nützlichsten Informationen.

Die Abstimmung wird von Briefcase initiiert, wenn festgelegt wird, dass sich mindestens zwei Kopien desselben Dokuments unterscheiden. In Aktentasche, das in diesem Kontext als Initiator fungiert, wird die dem angegebenen Dokumenttyp zugeordnete Aktentasche-Synchronisierung nach dem jeweiligen Dokumenttyp lokalisiert und gestartet. Die Synchronisierung vergleicht die Dokumente und bestimmt, welche Teile der Dokumente beibehalten werden. Einige Konflikt Handler erfordern möglicherweise eine Benutzerinteraktion, um die Abstimmung abzuschließen. Andere Benutzer können die Abstimmung ohne Benutzerinteraktion durchführen. Die Synchronisierung kann in einer Anwendung enthalten sein oder eine Erweiterung sein, die als dll implementiert ist.

Einige brieffall-Abgleiche können zu Daten Rückständen führen. Ein Rückstand ist ein Dokument, das in der Regel den gleichen Dateityp wie das ursprüngliche Dokument hat, das Informationen enthält, die nicht in der zusammengeführten Version gespeichert wurden. Mithilfe von-Nachrichten können Autoren in der Regel schnell feststellen, welche Informationen aus Ihrem ursprünglichen Dokument nicht in der endgültigen zusammengeführten Version enthalten sind. Wenn ein-Abgleichen von Rückständen unterstützt wird, erstellt er einen Rückstand für jede der ursprünglichen Versionen des Dokuments. Es werden keine Reste erstellt, es sei denn, der Initiator fordert Sie an

Einige Brief Synchronisierer von Brief Fällen können mit Aktentasche verwendet werden, damit der Benutzer die Abstimmung beenden kann. Dies ist eine wichtige Funktion für einen Benutzer, der sich entscheiden kann, dass die Abstimmung nicht fortgesetzt werden soll. Eine Abstimmung stellt in der Regel ein Beendigungs Objekt bereit, wenn die Abstimmung eine Benutzerinteraktion erfordert und lange dauern kann. In einigen Umgebungen kann eine Abstimmung eine partielle Abstimmung zulassen, sodass ein Benutzer eine Abstimmung vorübergehend aussetzen und später wieder fortsetzen kann. "Briefcase" unterstützt derzeit keine partielle Abstimmung.

### <a name="creating-a-briefcase-reconciler"></a>Erstellen eines Briefcase-abversers

Sie erstellen eine Aktentasche-Abstimmung, indem Sie die ababstimmungs Schnittstellen implementieren. Ein-connecler implementiert mindestens die [**ireconcilableobject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) -Schnittstelle und die [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) -oder [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle. Als Initiator bestimmt Briefcase, wann eine Abstimmung erforderlich ist, und ruft die [**ireconcilableobject::**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) abstimmen-Methode auf, um die Abstimmung zu initiieren.

Obwohl [**ireconcilableobject::**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) abgestimmt einen umfangreichen Satz von abgleichsfunktionen bereitstellt, führt eine Aktentasche-Abstimmung in den meisten Fällen nur minimale Abstimmung durch. Insbesondere ist es für Briefcase nicht erforderlich, dass die Abkopplung die Rückstands Generierung unterstützt oder das Beendigungs Objekt unterstützt. Die Abstimmung führt außerdem eine einzige von oben nach unten gerichteten Abstimmung durch und darf nicht den Wert "REC E notcomplete" zurückgeben, d \_ \_ . h., Sie sollte keine partielle Abstimmung versuchen.

Briefcase stellt die [**ireconcileinitiator**](ireconcileinitiator.md) -Schnittstelle bereit. Die Aktentasche-Vergleichsfunktion kann die [**ireconcileinitiator:: setabortcallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback) -Methode verwenden, um das Beendigungs Objekt festzulegen. "Briefcase" verwendet keine Versions Bezeichner und kann daher keine früheren Versionen eines Dokuments bereitstellen, wenn Sie von einem Vergleichsdienst mithilfe der entsprechenden Methoden in **ireconcileinitiator** angefordert werden.

Briefcase übergibt an [**ireconcilableobject::**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) ausgleichen dateimoniker, die die Versionen des zu stimmenden Dokuments darstellen. Die Aktentasche-Synchronisierung erhält Zugriff auf die Versionen, indem Sie entweder die [IMoniker:: bindteobject](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) -Methode oder die [IMoniker:: bindesstorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) -Methode verwendet. Letzteres ist im Allgemeinen schneller und wird empfohlen. Die Synchronisierung muss alle Objekte oder Speicher freigeben, an die Sie gebunden wird.

Wenn der Aktentasche-Verbindungs Dienst [IMoniker:: bindesstorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage)verwendet, wird er an einen Speicher gebunden, bei dem es sich entweder um einen flatstorage (einen Stream) oder einen OLE-definierten strukturierten Speicher handelt. Wenn für die Verbindung eine flache Speicherung erwartet wird, sollte IMoniker:: BindToStorage verwendet werden, um die [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Schnittstelle anzufordern. Wenn die-Konfiguration eine strukturierte Speicherung erwartet, sollte Sie die [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) -Schnittstelle anfordern. In beiden Fällen sollte Sie einen schreibgeschützten direkten (nicht transaktiven) Zugriff auf den Speicher anfordern. der Lese-/Schreibzugriff ist möglicherweise nicht verfügbar.

Ein minimaler Aktentasche-Vergleich sucht in der Regel direkt nach dem Speicher der anderen Versionen und verarbeitet eingebettete Objekte in sehr primitiver Weise, z. b. das Zusammenführen von zwei Versionen des Objekts durch einbeziehen beider Versionen in der Ausgabe Version.

Der Initiator sucht mithilfe einer Teilmenge der Logik, die von der [getclassfile](/windows/win32/api/objbase/nf-objbase-getclassfile) -Funktion implementiert wird, den Typ einer bestimmten Datei und sucht dann in der Registrierung nach der dem angegebenen Dateityp zugeordneten "Versöhnler"-Klasse. In Briefcase wird wie bei anderen Shellkomponenten der Dateityp ausschließlich durch die Dateinamenerweiterung bestimmt. Die Erweiterung einer Datei muss über einen registrierten Dateityp für "Briefcase" verfügen, um einen für die Datei abgleichen. Sie müssen einen Registrierungs Eintrag der folgenden Form festlegen, wenn Sie die-Synchronisierung installieren.

```
CLSID
   {the file CLSID}
      Roles
         Reconciler
            (Default) = {the reconciler-classid}
```

Die Klasse muss schnell geladen werden, muss \_ als multipleuse angegeben werden, und es muss sich um einen in-Process-Server (der in einer DLL enthalten ist) und nicht um einen lokalen Server (Implementiert in einer exe-Datei) handeln.

### <a name="user-interaction-in-reconciliation"></a>Benutzerinteraktion bei Abstimmung

Eine brieffall-Abstimmung sollte versuchen, eine Abstimmung ohne Benutzerinteraktion auszuführen. Umso automatisierter ist die Abstimmung des Benutzers.

In einigen Fällen kann der Benutzereingriff wertvoll sein. Beispielsweise kann ein Dokument System erfordern, dass ein Benutzer Änderungen überprüfen kann, bevor er die zusammengeführte Version eines Dokuments annimmt. es kann auch sein, dass Kommentare vom Benutzer erforderlich sind, die die vorgenommenen Änderungen erläutern. In diesen Fällen ist der Initiator, nicht der Buchstabe "Aktentasche", dafür verantwortlich, den Benutzer abzufragen und die Anweisungen des Benutzers auszuführen.

In anderen Fällen kann ein Benutzereingriff erforderlich sein, z. –., wenn zwei Versionen auf inkompatible Weise bearbeitet wurden. In solchen Fällen muss entweder der Initiator oder der Aktentasche-Konflikt Bezeichner den Benutzer Abfragen, um Anweisungen zum Beheben des Konflikts zu erhalten. Im Allgemeinen kann kein Initiator auf das Abschließen einer Abstimmung verlassen, ohne dass eine Benutzerinteraktion erwartet wird. Allerdings haben Sie die Möglichkeit, mit dem Benutzer zu interagieren, um Konflikte aufzulösen oder den Initiator zu erfordern.

### <a name="reconciling-embedded-objects"></a>Abgleichen von eingebetteten Objekten

Beim Abgleichen eines Dokuments kann die Aktentasche-Abstimmung selbst ein Initiator werden, wenn ein eingebettetes Objekt eines Typs erkannt wird, das nicht abgeglichen werden kann. In diesem Fall muss die Abstimmung jedes der eingebetteten Objekte rekursiv abstimmen und alle Verantwortlichkeiten eines Initiators annehmen.

Um die Rekursion auszuführen, lädt die Aktentasche-Konfiguration das Objekt und fragt die entsprechende Schnittstelle ab. Der-Handler für das-Objekt muss die-Schnittstelle unterstützen. Wenn eine Methode der Schnittstelle den OLE \_ E- \_ notrunning-Wert zurückgibt, muss das-Objekt das-Objekt ausführen, um den Vorgang auszuführen. Da Code für eingebettete Objekte nicht immer verfügbar ist, muss eine Problemlösung eine Lösung für diese Bedingung bereitstellen. Beispielsweise kann die-Vereinbarkeit sowohl alte als auch neue Versionen des eingebetteten Objekts in der abgeglichen Version enthalten. Die Abstimmung darf nicht versuchen, Verknüpfungen über Verknüpfungen abzustimmen.

Der Initiator speichert die Dokument Versionen, die zusammengeführt werden. In vielen Fällen hat der Initiator Zugriff auf den Speicher jeder Version und speichert das Ergebnis der Abstimmung mithilfe eines ähnlichen Speichers. Manchmal verfügt der Initiator jedoch möglicherweise über ein in-Memory-Objekt, für das keine persistente Version verfügbar ist. Diese Situation kann auftreten, wenn ein Dokument mit geöffneten eingebetteten Objekten abgestimmt werden muss, bevor es gespeichert wird. In solchen Fällen speichert der Initiator das Ergebnis der Abstimmung in der Version, die im Arbeitsspeicher gefunden wird.

Der Initiator verwendet die [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) -Schnittstelle, um die zusammengeführte Version zu binden (laden). Der Initiator verwendet die [IPersistStorage:: Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) -Methode, wenn bereits eine anfängliche Version erstellt wurde, und verwendet die [IPersistStorage:: InitNew](/windows/win32/api/objidl/nf-objidl-ipersiststorage-initnew) -Methode für die anfängliche Version. Wenn die zusammengeführte Version geladen wird, verwendet der Initiator [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , um die Adresse der [**ireconcilableobject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) -Schnittstelle abzurufen. Diese Schnittstelle ermöglicht dem Initiator den Zugriff auf die Speicherung der vorhandenen-Rest-und bietet eine Möglichkeit zum Erstellen von Speicherplatz für alle neuen-Rest-Geräte. Anschließend leitet der Initiator die-Schnittstelle an, um die Abstimmung auszuführen. Der Initiator fragt tatsächlich die [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle vor IPersistStorage ab. Wenn die-Methode IPersistFile unterstützt, manipuliert der Initiator das Replikat über die IPersistFile-Methode anstelle der IPersistStorage-Methoden. Dies ermöglicht die Abstimmung von Dateien, die nicht als Verbund Dokumente gespeichert werden.

Wenn die Abstimmung vollständig ist, kann der Initiator die zusammengeführte Version mithilfe der [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) -oder [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle speichern. Während der Abstimmung erstellt der Aktentasche-Konflikt die nach Bedarf, und schreibt die persistenten Bits in den Speicher. Wenn die zusammengeführte Version ein Stream ist, enthält die an [IPersistStorage:: Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) über gegebene [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) -Schnittstelle einen Stream mit dem Namen "Content", wobei der Speicherstatus auf statebits Flat festgelegt ist \_ . (Sie können die Zustands Bits mithilfe der [IStorage:: stat](/windows/win32/api/objidl/nf-objidl-istorage-stat) -Methode festlegen.) Nach der Zusammenführung speichert der Initiator die zusammengeführte Version, indem er die Daten in angemessener Weise schreibt. Dabei sollte sichergestellt werden, dass statebits \_ Flat für den Speicher entsprechend festgelegt ist.

### <a name="residues"></a>Stoff

Der Initiator gibt an, ob die Daten Rückstände durch Festlegen des Parameters *pstgnew-Rest* auf eine gültige Adresse beim Aufrufen der [**ireconcilableobject::**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) Rename-Methode festgelegt werden sollen. Wenn die-Abstimmung die Erstellung von-Replikate nicht unterstützt, muss Sie sofort den Wert von "REC \_ E \_ noresidues" zurückgeben, es sei denn, der *dwFlags* -Parameter gibt den Wert für den Wert der **\_** Eigenschaft "" von "Wert"

Die Aktentasche-Synchronisierung gibt durch Erstellen neuer Speicherelemente und Kopieren in das Array, auf das von *pstgnewreturns* verwiesen wird, Rückstände an den Initiator zurück. Bei strukturierten Speicher Rückständen kopiert der Verbindungs Dienst eine [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) -Schnittstelle, und bei flachen Speicher Rückständen wird entweder eine [IStream](/windows/win32/api/objidl/nn-objidl-istream) -oder eine IStorage-Schnittstelle mit dem festgelegten statebits- \_ Flag kopiert. Der-Abgleich verwendet IStorage, um den erforderlichen Speicher zu erstellen, wobei [IStorage:: foratestream](/windows/win32/api/objidl/nf-objidl-istorage-createstream) verwendet wird, um einen flachen Speicher für einen Restwert zu erstellen, bei dem es sich um einen Stream und [IStorage:: foratestorage](/windows/win32/api/objidl/nf-objidl-istorage-createstorage) handelt

Der Initiator bereitet *pstgnewrückstände* vor, sodass keine Elemente im nicht reservierten Teil des [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) -Namespace enthalten sind. Die Aktentasche-Synchronisierung platziert jeden Rest in einem Element, dessen Name der Reihenfolge ihrer ursprünglichen Version entspricht. Beispielsweise ist der erste Rest in "1", der zweite in "2" usw. enthalten. Wenn das abgeglichen Objekt selbst einen Rückstand erzeugt, befindet es sich im-Element mit dem Namen "0".

Die Aktentasche-debuggung führt ein Commit für jedes der neu erstellten Elemente einzeln aus, um sicherzustellen, dass der Initiator auf die Informationen zugreifen kann. Die-Synchronisierung führt jedoch kein Commit für *pstgnewrest* -Objekte aus. Der Initiator ist dafür verantwortlich, diesen Commit auszuführen oder anderweitig zu verwerfen.

## <a name="briefcase-reconciler-reference"></a>Referenz zur Briefcase-Synchronisierung

Dieser Abschnitt enthält Informationen zu den Abstimmungs Schnittstellen. Bei der Behandlung von Fehlern kann eine Methode nur die Fehler Werte zurückgeben, die explizit als mögliche Rückgabewerte definiert sind. Außerdem muss die-Methode alle Variablen festlegen, deren Adressen als Parameter an **null** weitergegeben werden, bevor der Fehler zurückgegeben wird.

### <a name="briefcase-reconciler-interfaces-and-methods"></a>Schnittstellen und Methoden der Briefcase-Synchronisierung

-   [**Ireconcilableobject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) 
    -   -   [**Ireconcilableobject:: getprogressfeedbackmaxschätz**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-getprogressfeedbackmaxestimate)
        -   [**Ireconcilableobject:: Abstimmung**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile)

-   [**Ireconcileinitiator**](ireconcileinitiator.md) 
    -   -   [**Ireconcileinitiator::-tabortcallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)
        -   [**Ireconcileinitiator:: setprogressfeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback)

-   [**Inotifyreplica**](/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica) 
    -   -   [**Inotifyreplica:: youareareplica**](/windows/desktop/api/reconcil/nf-reconcil-inotifyreplica-youareareplica)

 

 