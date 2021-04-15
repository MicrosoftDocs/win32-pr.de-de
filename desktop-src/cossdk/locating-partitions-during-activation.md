---
description: Suchen von Partitionen während der Aktivierung
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: Suchen von Partitionen während der Aktivierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104569782"
---
# <a name="locating-partitions-during-activation"></a>Suchen von Partitionen während der Aktivierung

Das Auffinden der richtigen Partition, in der eine Komponente aktiviert werden soll, hängt von folgendem ab:

-   Der Funktionsaufruf und die Parameter, die im aufrufenden Programm zum Aktivieren der Komponente verwendet werden.
-   Gibt an, ob die aktivierte Komponente lokal oder Remote ist.
-   Die interne Verwendung des Partitions Caches

## <a name="the-calling-program"></a>Das Aufruf Programm

Com+ wählt die Partition für die Komponenten Aktivierung basierend darauf aus, wie das aufrufenden Programm die Komponente aktiviert.

Es gibt drei verschiedene Aktionen, die com+ durchführen kann, wenn eine Partition für die Komponenten Aktivierung ausgewählt wird. Die ausgeführte Aktion hängt davon ab, wie das aufrufende Programm das Objekt instanziiert, das heißt, ob der Funktionsaufruf einen partitionmoniker enthält, der aus einer Partitions-ID und einer CLSID besteht, oder nur eine CLSID enthält.

In der folgenden Tabelle sind die verschiedenen Aktionen aufgeführt, die com+ in der Rangfolge durchführen kann, um eine Partition zu suchen.



| Funktionsaufruf                                                  | Parameter                                                      | Com+-Aktion                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) oder **GetObject**<br/> | Partitionsmoniker (einschließlich Partitions-ID und CLSID)<br/> | Verwendet die im partitionsmoniker angegebene Partitions-ID.<br/>                                                                                                                           |
| [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | CLSID<br/>                                               | Verwendet entweder die Partitions-ID der Standard Partition der Benutzeridentität oder die Partitions-ID, die dem Kontext während einer vorherigen Komponenten Aktivierung im selben Prozess hinzugefügt wurde.<br/> |



 

Die in der obigen Tabelle aufgeführten com+-Aktionen werden in den folgenden Abschnitten erläutert.

## <a name="use-of-partition-monikers"></a>Verwendung von partitionmonikern

Eine Partition kann innerhalb eines Funktions Aufrufes mithilfe eines *partitionsmonikers* explizit ausgewählt werden. Ein partitionsmoniker wird im Code verwendet, um die Partition der aktivierten Komponente explizit anzugeben. Wenn ein partitionsmoniker zum Auffinden der Partition verwendet wird, erfolgt die Aktivierung von dieser Partition. Das heißt, die Partitions-ID, die im Moniker enthalten ist, hat Vorrang vor der Standard Partition des Benutzers oder über eine Partitions-ID, die im Kontext des Aufrufers vorhanden ist.

In C++-Code lautet die Syntax für die Verwendung eines partitionsmonikers wie folgt:


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



Das folgende Beispiel zeigt einen Code Ausschnitt von C++-Code, in dem ein partitionsmoniker als Argument für die [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) -Funktion verwendet wird:


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



In Visual Basic Code lautet die Syntax für einen partitionsmoniker wie folgt:


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



Das folgende Beispiel zeigt einen Ausschnitt von Visual Basic-Code, in dem ein partitionsmoniker als Argument für die **GetObject** -Funktion verwendet wird:


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a>Verwendung der Standard Zuordnung

Wenn die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion verwendet wird, um eine Komponente mithilfe der CLSID der Komponente zu aktivieren, verwendet com+ die standardmäßige Benutzer Identitäts Zuordnung, d. h. den Partitions Satz, dem der Benutzer in Active Directory zugeordnet ist. Wenn der Benutzer jedoch keinem in Active Directory zugeordneten Partitions Satz zugeordnet ist, wird die globale Partition ausgewählt.

## <a name="use-of-partition-ids-and-object-context"></a>Verwendung von Partitions-IDs und Objekt Kontext

Eine der fünf Eigenschaften, die einer neuen Partition zugewiesen ist, ist die Partitions-ID. Wenn das Client Programm die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufruft, um ein Objekt zu instanziieren, wird die Partitions-ID dem Kontext hinzugefügt. Die Verwendung der Partitions-ID aus dem Kontext zum Suchen der Partition ist wichtig, da sie sicherstellt, dass nach Beginn einer Kette von Aktivierungen die Partitions-ID unverändert bleibt, es sei denn, Sie wird explizit durch einen partitionmoniker geändert.

Weitere Informationen zum Suchen von Partitionen während der Aktivierung finden Sie unter [com+-in der Warteschlange befindliche Komponenten und Partitionen](com--queued-components-and-partitions.md).

## <a name="local-and-remote-activation"></a>Lokale Aktivierung und Remote Aktivierung

-   Wenn die aufgerufene Komponente auf einem anderen Computer vorhanden ist, werden die Partitions Eigenschaften (einschließlich der Partitions-ID) an den anderen Computer gemarshallt, und die Komponente wird von der gemarshallten Partition aus aktiviert. Wenn keine Partitions-ID gemarshallt wurde, verwendet com+ den Standard Partitions Satz, der der Benutzeridentität in Active Directory zugeordnet ist.

## <a name="the-partition-cache"></a>Der Partitions Cache

In einer Domänen Umgebung verwendet com+ die Zuordnungen in Active Directory, um die richtige Partition für die Komponenten Aktivierung zu suchen. Häufige Suchvorgänge in Active Directory können jedoch zu einem übermäßigen Netzwerkverkehr führen. Um den Netzwerk Datenverkehr zu minimieren, der sich aus häufigen suchen der Zuordnung zwischen Benutzern und Partitionen in Active Directory ergibt, verwendet com+ einen *Partitions Cache*.

Der Partitions Cache enthält die Zuordnungen, die in Active Directory zwischen Benutzer Identitäten oder Organisationseinheiten und deren Partitions Sätzen vorgenommen wurden. Dieser Partitions Cache befindet sich auf dem Anwendungsserver, auf dem sich die com+-Anwendungen befinden.

Wenn com+ die Standard Partition eines Benutzers bestimmen oder die Zugriffsrechte eines Benutzers auf eine Partition überprüfen muss, wird der Partitions Cache lokal überprüft, um die Zuordnung des Benutzers zu überprüfen, anstatt Active Directory Remote zu überprüfen.

Wenn die Suche im Partitions Cache fehlschlägt, prüft com+ Active Directory. Wenn die Suche in Active Directory erfolgreich ist, speichert com+ diese Zuordnung im Partitions Cache. Wenn Sie das nächste Mal eine Suche für die Zuordnung zwischen Benutzern und Partitionen durchführt, wird Sie von com+ im Partitions Cache gefunden.

Die folgende Abbildung zeigt den Prozess, den com+ verwendet, um eine Partition für die Komponenten Aktivierung zu suchen.

![Diagramm, das eine Problem Behandlungs Struktur für den Prozess anzeigt, den com+ zum Suchen einer Partition für die Komponenten Aktivierung verwendet.](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

Die Größe des Caches und die Ablaufzeit für die Cache Einträge werden über Registrierungsschlüssel festgelegt. Weitere Informationen zum Konfigurieren dieser Registrierungsschlüssel finden Sie unter [Erstellen und Konfigurieren von COM+-Partitionen](creating-and-configuring-com--partitions.md).

> [!Note]  
> Wenn ein Server Computer vom Netzwerk getrennt ist und die Zuordnung zwischen Benutzer und Partition geändert wird, während der Server getrennt wird, kann der Partitions Cache eine veraltete Zuordnung zwischen Benutzern und Partitionen enthalten. Dies kann zu einem Aktivierungs Fehler führen, wenn die Zuordnung zwischen Benutzer und Partition der Mechanismus ist, der zum Aktivieren einer Komponente verwendet wird.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Suchen einer Komponente zur Aktivierung](locating-a-component-for-activation.md)
</dt> </dl>

 

