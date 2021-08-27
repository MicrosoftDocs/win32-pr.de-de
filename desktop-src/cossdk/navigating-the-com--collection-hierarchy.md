---
description: Navigieren in der COM+-Sammlungshierarchie
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Navigieren in der COM+-Sammlungshierarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef6f23cd9f584b6cbe496fe7122abfa9978cd25cb28d81a5c89782b718138be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070450"
---
# <a name="navigating-the-com-collection-hierarchy"></a>Navigieren in der COM+-Sammlungshierarchie

Einige Sammlungen, die Sie problemlos abrufen können, indem Sie die [**GetCollection-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) für das [**COMAdminCatalog-Objekt**](comadmincatalog.md) verwenden. Diese Methode ruft eine Auflistung der obersten Ebene ab. Das heißt, eine Sammlung wie [**Applications**](applications.md), die eigenständig steht und eindeutig ist und nicht logisch unter einer anderen Auflistung untergliedert ist.

Viele Auflistungen werden jedoch logisch unter einer anderen Auflistung subsumiert, da sie Elemente enthalten, die Teil einer größeren Struktur sind. Beispielsweise wird die [**Components-Auflistung**](components.md) mit der [**Applications-Auflistung**](applications.md) subsumiert oder verknüpft, da sie die Komponenten enthält, die in einer bestimmten COM+-Anwendung installiert sind, die selbst einem Element in der **Applications-Auflistung** entspricht. Verwandte Sammlungen wie diese sind nicht eindeutig. es gibt eine **Components-Auflistung** für jede unterschiedliche Anwendung.

Daher werden Auflistungen in einer hierarchischen Struktur angeordnet, die natürlich den logischen Beziehungen zwischen den elementen entspricht, die sie enthalten. Ein Diagramm der Sammlungshierarchie finden Sie unter [COM+-Verwaltungssammlungen.](com--administration-collections.md) Für viele der Elemente, die Sie mithilfe der COMAdmin-Objekte konfigurieren möchten, müssen Sie durch einen Teil der Sammlungshierarchie navigieren, um das entsprechende Element abzurufen.

Dies bedeutet in der Praxis, dass Sie, wenn Sie ein Element in einer verknüpften Sammlung abrufen möchten, zuerst alle erforderlichen übergeordneten Ebenen durchlaufen und Sammlungen aufzählen müssen. Um eine verknüpfte Auflistung abzurufen, müssen Sie das spezifische Element in der übergeordneten Auflistung abrufen, mit dem die untergeordnete Auflistung verknüpft ist. Wenn Sie beispielsweise ein Element konfigurieren möchten, das einer Komponente in einer bestimmten COM+-Anwendung entspricht, müssen Sie die folgenden Schritte ausführen:

1.  Abrufen der [**Applications-Sammlung**](applications.md) und Auffüllen.
2.  Aufzählen sie den Inhalt [](applications.md) der Anwendungsauflistung, bis Sie zu dem Element gelangen, das der richtigen COM+-Anwendung entspricht.
3.  Abrufen und Auffüllen der [**Components-Auflistung**](components.md) für diese bestimmte COM+-Anwendung.
4.  Aufzählen sie den Inhalt der [**Components-Auflistung,**](components.md) bis Sie zu dem Element gelangen, das der richtigen Komponente entspricht.

Im folgenden Microsoft Visual Basic Beispiel wird gezeigt, wie die vorherigen Schritte ausgeführt werden:


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



Im vorherigen Beispiel werden zwei unterschiedliche **GetCollection-Methoden** verwendet. Die erste wird von [**COMAdminCatalog**](comadmincatalog.md) verfügbar gemacht und zum Abrufen einer Sammlung der obersten Ebene verwendet, in diesem Fall "Anwendungen". Die zweite wird von [**COMAdminCatalogCollection**](comadmincatalogcollection.md) verfügbar gemacht und zum Abrufen einer Sammlung verwendet, die sich auf die aktuelle Sammlung bezieht. Sie geben genau an, welche Sammlung Sie verwenden möchten, indem Sie den Namen "Components" und den Key-Eigenschaftswert des übergeordneten Objekts übergeben. Der Key-Eigenschaftswert ist häufig ein Name oder eine GUID, die das Objekt eindeutig identifiziert. dieser Wert wird in der Dokumentation für jede Sammlung identifiziert.

Im allgemeinen Fall müssen Sie verwandte Sammlungen iterativ in der Sammlungshierarchie abrufen, bis Sie die gewünschte Sammlung abrufen. Die Schritte, die Sie ausführen würden, folgen wiederholt dem gleichen allgemeinen Modell. Eine vollständige Liste der Sammlungen finden Sie unter [COM+-Verwaltungssammlungen.](com--administration-collections.md)

In einigen Fällen möchten Sie möglicherweise eine Verknüpfungsmethode verwenden, wenn Sie ein zweites Mal einem Pfad durch die Auflistungshierarchie folgen. Sie können diese Methode nur verwenden, nachdem Sie alle dazwischen liegenden Schlüsselwerte bereits zwischengespeichert haben. Weitere Informationen finden Sie unter [**ICOMAdminCatalog::GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auffüllen von COM+-Sammlungen](populating-com--collections.md)
</dt> <dt>

[Abfragen verfügbarer verwandter Sammlungen](querying-for-available-related-collections.md)
</dt> <dt>

[Abrufen von Sammlungen im COM+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



