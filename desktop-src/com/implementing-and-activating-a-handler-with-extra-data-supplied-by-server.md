---
title: Implementieren und Aktivieren eines Handlers mit zusätzlichen Daten, die vom Server bereitgestellt werden
description: Implementieren und Aktivieren eines Handlers mit zusätzlichen Daten, die vom Server bereitgestellt werden
ms.assetid: 5bbf81bd-430d-4008-b1cc-9ea91bb3b1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78a3e39c85c37c52dfa3f09ef41f0a71b5f431
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104350868"
---
# <a name="implementing-and-activating-a-handler-with-extra-data-supplied-by-server"></a>Implementieren und Aktivieren eines Handlers mit zusätzlichen Daten, die vom Server bereitgestellt werden

Wenn der Server zusätzliche Daten in das Paket aufnehmen möchte, die der Handler verwenden soll, muss der Server sowohl die [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) -als auch die [**istdmarshalinfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) -Schnittstelle implementieren. Der Server muss den standardmarshaler aggregieren und den ersten Teil des Marshalling an den aggregierten Standard-Mars Haller, einschließlich [**IMarshal:: GetUnmarshalClass**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getunmarshalclass), delegieren und seine eigene Datengröße der Größe hinzufügen, die vom standardmäßigen Mars Haller [**:: GetMarshalSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getmarshalsizemax)zurückgegeben wird. Der Standard-Mars Haller ruft [**istdmarshalinfo:: getclassforhandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler) auf, um die CLSID des zu erstellenden Handlers zu erhalten. Nachdem der Standard-Mars Haller das Marshalling abgeschlossen hat, schreibt der Server seine eigenen zusätzlichen Daten in den Stream. Die resultierenden Strukturen mit zusätzlichen Daten im Stream werden in der folgenden Abbildung dargestellt:

![Diagramm, das Strukturen mit zusätzlichen Daten im Stream anzeigt.](images/4cff306b-bb82-4c05-8e64-7ca73731f265.png)

## <a name="server-side-structures-with-extra-data-in-stream"></a>Server-Side Strukturen mit zusätzlichen Daten im Stream

Dies ermöglicht es dem com- [**ansichtinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) , auf der Clientseite alle ungelesenen Daten zu überspringen und den Stream nach allen gemarshallten Schnittstellen Daten an der entsprechenden Position zu belassen, wenn der Handler nicht erstellt werden kann.

## <a name="client-side-structures-with-extra-data-in-stream"></a>Client-Side Strukturen mit zusätzlichen Daten im Stream

Wie in dem Fall, in dem keine zusätzlichen Serverdaten im Stream vorhanden sind, erstellt der Client seitige com-Befehl von " [**zählmarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) " die Identität und den Handler. Der Handler muss die Methode " [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) " implementieren und die **IMarshal** -Aufrufe zuerst an den aggregierten Standard-Mars Haller delegieren und dann alle zusätzlichen Daten, die der Server bereitgestellt hat, Mars Hallen bzw. aus dem Mars Hallen. Die [**UnmarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-unmarshalinterface) -Methode des Handlers wird für jedes unmars Hall aufgerufen, unabhängig davon, ob die Schnittstelle vor oder nach dem Marshalling von ihr gemarshallt wurde. In diesem Fall ruft der Server nicht [**cogetstdmarshalex**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) auf, aber der Handler muss. Die resultierende Client seitige Struktur wird in der folgenden Abbildung dargestellt.

![Diagramm, das die Client seitige Struktur anzeigt.](images/053411c7-9d54-4ae5-bcb6-778454b1d86f.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Der Lightweight Client-Side-Handler](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 