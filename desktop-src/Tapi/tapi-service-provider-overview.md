---
description: TAPI-Anwendungen befinden sich in Ihrem eigenen Prozessbereich.
ms.assetid: 57dedad1-7264-48fc-9ac2-c6c72f7fee27
title: TAPI-Dienstanbieter (Übersicht)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e847ed49879e9ff55662477a762fa7297443d12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571666"
---
# <a name="tapi-service-provider-overview"></a>TAPI-Dienstanbieter (Übersicht)

TAPI-Anwendungen befinden sich in Ihrem eigenen Prozessbereich. TAPI-Anwendungen laden die Tapi32.dll oder Tapi3.dll in Ihren Prozess, und TAPI kommuniziert mit tapisrv über eine private RPC-Schnittstelle. Ein TSP wird im Kontext von tapisrv ausgeführt. Ein bestimmter TSP kann sich auf einem anderen Computer als dem Computer des Benutzers befinden, und der Zugriff erfolgt über einen Remote-TSP. Tapisrv ist als Dienst Prozess innerhalb von svchost implementiert. Ein MSP befindet sich im Prozessbereich der Anwendung und ist immer lokal.

Ein TSP/MSP-Paar kann als einen virtuellen privaten Kommunikations Pfad angesehen werden. Informationen können zwischen den beiden mithilfe von nicht transparenten Puffern gesendet werden, die weder von tapisrv noch von der TAPI-dll interpretiert werden.

Einige Dienstanbieter implementieren spezifische Vorgänge für die betreffende Hardware. TAPI 2. x ermöglicht den Zugriff auf solche Vorgänge über die [**linedevspecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) -oder [**phonedevspecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) -Funktion. TAPI 3. x macht [anbieterspezifische Schnittstellen](./provider-specific-interfaces.md)verfügbar.

Das folgende Diagramm veranschaulicht den Ablauf von Steuerelementen und Informationen, die einen eigenständigen TSP (Unimodem) und ein TSP/MSP-Paar (H. 323) zeigen.

![eigenständiger TSP und gekoppelter TSP/MSP-Ablauf Steuerung und-Informationen](images/tsp-msp1.png)

Das folgende Diagramm veranschaulicht den Fortschritt eines eingehenden-Aufrufes, der sowohl einen TSP als auch einen MSP umfasst.

![eingehender Rückruf mit einem TSP und einem msp](images/tspmspin.png)

## <a name="incoming-call-setup"></a>Setup für eingehende Anrufe

-   Der TSP sendet eine [**Zeile \_ newcallnachricht**](line-newcall.md) an tapisrv. Der [**Status des Aufrufes**](./linecallstate--constants.md) ist linecallstate- \_ Angebot.
-   Tapisrv benachrichtigt Clients über den-Rückruf.
-   Tapi3 erstellt das TAPI-Aufruf Objekt und ruft dann [**itmspaddress:: deatemspcallauf**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-createmspcall), das vom MSP implementiert wird.
-   Der MSP erstellt basierend auf den für den-aufrufbedarf erforderlichen [**Medientypen**](./tapimediatype--constants.md) ein MSP-aufrufsobjekt und Standarddaten Ströme. Er gibt einen IUnknown-Zeiger auf das MSP-aufrufsobjekt zurück.
-   Tapi3 aggregiert das MSP-aufrufsobjekt in das TAPI-anrufsobjekt und macht Schnittstellen wie [**itstreamcontrol**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) für die Anwendung verfügbar. Anschließend wird die Anwendung über den neuen-Befehl benachrichtigt.

Die Anwendung kann dann Methoden wie z. [**b. itstream:: selectterminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) verwenden, um die Vorbereitung für die Beendigung des Aufrufes abzuschließen

## <a name="incoming-call-completion"></a>Eingehende Rückruf Ausführung

-   Die Anwendung ruft [**itbasiccallcontrol:: answer**](/windows/win32/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer)auf.
-   Tapi3 ruft [**lineanswer**](/windows/win32/api/tapi/nf-tapi-lineanswer)auf.
-   Tapiserv ruft [**TSPI \_ lineanswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)auf.
-   Der TSP initiiert das Streaming von anrufen. Normalerweise sendet der TSP eine Nachricht an den entsprechenden msp, und der MSP startet die Datenströme. Bei einigen TSP-/MSP-Implementierungen startet der TSP die Datenströme.

## <a name="tspmsp-communication-during-call-progress"></a>TSP/MSP-Kommunikation während des Aufrufstatus

Nachdem der-Vorgang ausgeführt wurde, kommunizieren der TSP und der MSP durch das Übergeben von nicht transparenten Puffern über tapisrv und tapi3.

-   Der TSP sendet Informationen an den MSP, indem er [**die \_ sendmspdata-Zeilen**](line-sendmspdata.md) Nachricht an tapisrv sendet.
-   Der MSP empfängt Informationen aus dem TSP über die [**itmspaddress:: receivetspdata**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-receivetspdata) -Methode. Wenn die Daten mit einem MSP-aufrufsobjekt verknüpft sind, wird ein Schnittstellen Zeiger auf das MSP-aufrufen-Objekt als Parameter dieser Methode bereitgestellt.
-   Der MSP sendet Informationen an den TSP, indem er ein MSP \_ TSP- \_ Daten Ereignis an TAPI 3 sendet.
-   Der TSP empfängt Informationen aus dem MSP über die [**TSPI \_ linereceivemspdata**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata) -Funktion.

Der genaue Prozess und der Inhalt der Kommunikation zwischen Dienstanbietern sind spezifisch für einen bestimmten TSP/MSP-Satz.

> [!Note]  
> Bei ausgehenden Aufrufen kennt das MSP in der Regel den Aufruf vor dem TSP. Wenn der MSP versucht, mit dem TSP zu kommunizieren, bevor der TSP über einen-Rückruf informiert wird, schlägt die Kommunikation fehl. Wenn der MSP und der TSP Informationen zu einem bestimmten-Befehl austauschen müssen, sollte der TSP die Kommunikation initiieren.

 

 

 
