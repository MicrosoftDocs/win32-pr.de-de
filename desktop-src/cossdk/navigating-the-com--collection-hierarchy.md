---
description: Navigieren in der com+-Sammlungs Hierarchie
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Navigieren in der com+-Sammlungs Hierarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fc4cde6c56bc08b0326e892409067759e91be6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339689"
---
# <a name="navigating-the-com-collection-hierarchy"></a>Navigieren in der com+-Sammlungs Hierarchie

Einige Auflistungen, die Sie problemlos abrufen können, indem Sie die [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) -Methode für das [**comadmincatalog**](comadmincatalog.md) -Objekt verwenden. Diese Methode ruft eine Auflistung der obersten Ebene ab. Das heißt, eine Auflistung, z. b. [**Anwendungen**](applications.md), die eigenständig ist und eindeutig und in keiner anderen Auflistung logisch unterteilt ist.

Viele Auflistungen werden jedoch in einer anderen Auflistung logisch unterteilt, weil Sie Elemente enthalten, die Teil einer größeren Struktur sind. Beispielsweise wird die [**Komponenten**](components.md) Auflistung mit der [**Anwendungs**](applications.md) Auflistung subsumed oder verknüpft, da Sie die Komponenten enthält, die in einer bestimmten COM+-Anwendung installiert sind, die wiederum einem Element in der **Anwendungs** Auflistung entspricht. Verwandte Auflistungen wie diese sind nicht eindeutig. für jede einzelne Anwendung gibt es eine **Komponenten** Sammlung.

Daher werden Auflistungen in einer hierarchischen Struktur angeordnet, die auf natürliche Weise den logischen Beziehungen zwischen den darin enthaltenen Elementen entspricht. Ein Diagramm der Sammlungs Hierarchie finden Sie unter [com+-Verwaltungs Sammlungen](com--administration-collections.md). Für viele der Elemente, die Sie mit den COMAdmin-Objekten konfigurieren möchten, müssen Sie durch einen Teil der Sammlungs Hierarchie navigieren, um das entsprechende Element abzurufen.

Dies bedeutet in der Praxis, dass Sie, wenn Sie ein Element in einer verknüpften Auflistung erhalten möchten, alle erforderlichen höheren Ebenen durchlaufen müssen. Zum Abrufen einer verknüpften Auflistung müssen Sie das spezifische Element in der übergeordneten Auflistung abrufen, mit der die untergeordnete Auflistung verknüpft ist. Wenn Sie z. b. ein Element konfigurieren möchten, das einer Komponente in einer bestimmten COM+-Anwendung entspricht, müssen Sie die folgenden Schritte ausführen:

1.  Holen Sie sich die [**Anwendungs**](applications.md) Auflistung, und füllen Sie Sie auf.
2.  Durchlaufen Sie den Inhalt der [**Anwendungs**](applications.md) Auflistung, bis Sie zu dem Element gelangen, das der richtigen COM+-Anwendung entspricht.
3.  Rufen Sie die [**Komponenten**](components.md) Auflistung für die jeweilige COM+-Anwendung ab, und füllen Sie Sie auf.
4.  Durchlaufen Sie den Inhalt der [**Komponenten**](components.md) Auflistung, bis Sie zu dem Element gelangen, das der richtigen Komponente entspricht.

Im folgenden Microsoft Visual Basic Beispiel wird gezeigt, wie die vorangegangenen Schritte ausgeführt werden:


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



Im vorherigen Beispiel werden zwei unterschiedliche **GetCollection** -Methoden verwendet. Der erste wird durch [**comadmincatalog**](comadmincatalog.md) verfügbar gemacht und wird verwendet, um eine Sammlung der obersten Ebene zu erhalten – in diesem Fall "Applications". Die zweite wird durch [**comadmincatalogcollection**](comadmincatalogcollection.md) verfügbar gemacht und wird verwendet, um eine Auflistung zu erhalten, die mit der aktuellen Auflistung verknüpft ist. Sie geben genau die gewünschte Auflistung an, indem Sie den Namen "Components" und den Schlüssel Eigenschafts Wert des übergeordneten Objekts übergeben. Der Schlüssel Eigenschafts Wert ist oft ein Name oder eine GUID, die das Objekt eindeutig identifiziert. Dieser Wert wird in der Dokumentation für jede Sammlung identifiziert.

In den meisten Fällen müssen Sie verwandte Auflistungen iterativ in der Sammlungs Hierarchie abrufen, bis Sie die gewünschte Sammlung abrufen. Die Schritte, die Sie durchführen würden, folgen dem gleichen allgemeinen Modell, wiederholt. Eine komplette Liste der Sammlungen finden Sie unter [com+-Verwaltungs Sammlungen](com--administration-collections.md).

In einigen Fällen möchten Sie möglicherweise eine Verknüpfungs Methode verwenden, wenn Sie ein zweites Mal einen Pfad über die Auflistungs Hierarchie befolgen. Diese Methode kann nur verwendet werden, nachdem Sie bereits alle dazwischen liegenden Schlüsselwerte zwischengespeichert haben. Weitere Informationen finden Sie unter [**icomadmincatalog:: getcollectionbyquery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Sammlungen werden aufgefüllt.](populating-com--collections.md)
</dt> <dt>

[Abfragen von verfügbaren verwandten Sammlungen](querying-for-available-related-collections.md)
</dt> <dt>

[Abrufen von Auflistungen im com+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



