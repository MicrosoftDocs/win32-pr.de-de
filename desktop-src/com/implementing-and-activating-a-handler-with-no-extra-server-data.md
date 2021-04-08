---
title: Implementieren und Aktivieren eines Handlers ohne zusätzliche Server Daten
description: Implementieren und Aktivieren eines Handlers ohne zusätzliche Server Daten
ms.assetid: 9d91260a-4cec-4a10-bb57-d02999efae47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6866b40e1257a865aa5068ffd46611c411498877
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "103961043"
---
# <a name="implementing-and-activating-a-handler-with-no-extra-server-data"></a>Implementieren und Aktivieren eines Handlers ohne zusätzliche Server Daten

Wenn Sie eine Instanz Ihres Handlers erstellen möchten, die keine zusätzlichen Serverdaten erhält, muss der Server [**istdmarshalinfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) implementieren, aber nicht " [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)". **Istdmarshalinfo** verfügt über eine Methode, [**getclassforhandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler), die die CLSID des Objekt Handlers abruft, der im Ziel Prozess verwendet werden soll. COM ruft diese Methode auf, wenn Sie [**comarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) für Sie aufruft und den Handler auf der Clientseite aktiviert.

Als nächstes müssen sowohl die Server-als auch die Handlerimplementierungen die [**cogetstdmarshalex**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) -Funktion aufrufen. Diese Funktion erstellt auf jeder Seite einen Standard-Mars Haller (als Proxy-Manager auf der Clientseite und als Stub-Manager auf der Serverseite bezeichnet).

Der Server ruft [**cogetstdmarshalex**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)auf und übergibt dabei das Flag "smexf \_ Server". Dadurch wird ein serverseitiger Standard-Mars Haller (Stub-Manager) erstellt. Die serverseitige Struktur ist in der folgenden Abbildung dargestellt:

![Diagramm, das die serverseitige Struktur anzeigt.](images/b47b3bc0-3e7d-4be4-9767-7ae436bd1b21.png)

## <a name="server-side-structure"></a>Server-Side Struktur

Der Handler ruft " [**cogetstdmarshalex**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)" auf und übergibt dabei den Flag-"smexf"- \_ Handler. Dadurch wird ein Client seitiger Standard-Mars Haller (Proxy-Manager) erstellt und mit dem-Handler auf der Clientseite aggregiert. Die Lebensdauer von beidem wird vom Steuerungsobjekt verwaltet, das vom [**System implementiert wird**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), wenn der Handler **cogetstdmarshalex** aufruft. Die Client seitige Struktur ist in der folgenden Abbildung dargestellt.

![Diagramm, das die Client seitige Struktur anzeigt.](images/24ae70ef-dfa8-4784-90ac-dc6cfb043ee5.png)

## <a name="client-side-structure"></a>Client-Side Struktur

Wie in der obigen Abbildung gezeigt, wird der Handler tatsächlich zwischen dem Proxy-Manager und dem Identitäts-/kontrollierenden unbekannten eingebettet. Dadurch erhält das System die Kontrolle über die Lebensdauer des Objekts, während das handlersteuerelement über die verfügbar gemachten Schnittstellen verfügt. Die gestrichelte Linie zwischen der Identität und dem Proxy-Manager gibt an, dass die beiden die enge Integration über interne private Schnittstellen gemeinsam verwenden.

Wenn com für den Client die Methode " [**dinmarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) " aufruft, wird die Handlerinstanz erstellt und mit der Identität aggregierte. Der Handler erstellt den Standard-Mars Haller (durch Aufrufen von [**cogetstdmarshalex**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)und übergibt dabei den Steuerungs unbekannten, den er bei seiner Erstellung empfangen hat). Der Handler implementiert " [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) " nicht, sondern gibt nur " **IMarshal** " aus dem Standard-Marshaler zurück. Auch wenn der Handler " **IMarshal**" implementiert, wird er während eines unmars Hall nicht aufgerufen.

Wenn zwei Threads gleichzeitig das gleiche Objekt zum ersten Mal entsperren, kann es vorkommen, dass zwei Handler vorübergehend erstellt werden. Anschließend wird eine solche veröffentlicht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Der Lightweight Client-Side-Handler](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 