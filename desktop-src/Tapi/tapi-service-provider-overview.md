---
description: TAPI-Anwendungen befinden sich in ihrem eigenen Prozessbereich.
ms.assetid: 57dedad1-7264-48fc-9ac2-c6c72f7fee27
title: Übersicht über TAPI-Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29871b21124eab7ea4e7e84a9e7e8ca49853cb7a236c6f7a482dbf842a568304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760301"
---
# <a name="tapi-service-provider-overview"></a>Übersicht über TAPI-Dienstanbieter

TAPI-Anwendungen befinden sich in ihrem eigenen Prozessbereich. TAPI-Anwendungen laden die Tapi32.dll oder Tapi3.dll in ihren Prozess, und TAPI kommuniziert über eine private RPC-Schnittstelle mit TAPISRV. Ein TSP wird im Kontext von TAPISRV ausgeführt. Ein angegebener TSP kann sich auf einem anderen Computer als dem Computer des Benutzers befinden und über einen Remote-TSP darauf zugegriffen werden. TAPISRV wird als Dienstprozess in SVCHOST implementiert. Ein MSP befindet sich im Prozessbereich der Anwendung und ist immer lokal.

Ein TSP-/MSP-Paar kann als virtueller privater Kommunikationspfad betrachtet werden. Informationen können zwischen den beiden mithilfe von nicht transparenten Puffern gesendet werden, die weder von TAPISRV noch von der TAPI-DLL interpretiert werden.

Einige Dienstanbieter implementieren spezifische Vorgänge für die beteiligte Hardware. TAPI 2.x ermöglicht den Zugriff auf solche Vorgänge über die [**lineDevSpecific-**](/windows/win32/api/tapi/nf-tapi-linedevspecific) oder [**phoneDevSpecific-Funktion.**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) TAPI 3.x macht [anbieterspezifische Schnittstellen verfügbar.](./provider-specific-interfaces.md)

Das folgende Diagramm veranschaulicht den Fluss von Steuerelementen und Informationen und zeigt einen eigenständigen TSP (Unimodem) und ein TSP/MSP-Paar (H.323).

![eigenständiger TSP- und gekoppelter tsp/msp-Fluss von Steuerung und Informationen](images/tsp-msp1.png)

Das folgende Diagramm veranschaulicht den Fortschritt eines eingehenden Aufrufs, der sowohl einen TSP als auch einen MSP umfasst.

![Eingehender Anruf mit einem TSP und einem MSP](images/tspmspin.png)

## <a name="incoming-call-setup"></a>Einrichtung eingehender Anrufe

-   Der TSP sendet eine [**LINE \_ NEWCALL-Nachricht**](line-newcall.md) an TAPISRV. Der [**Aufrufzustand ist**](./linecallstate--constants.md) LINECALLSTATE \_ OFFERING.
-   TAPISRV benachrichtigt Clients über den Aufruf.
-   TAPI3 erstellt das TAPI Call-Objekt und ruft [**dann ITMSPAddress::CreateMSPCall**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-createmspcall)auf, das vom MSP implementiert wird.
-   Der MSP erstellt ein MSP Call-Objekt und Standardstreams basierend auf den für [**den**](./tapimediatype--constants.md) Aufruf erforderlichen Medientypen. Sie gibt einen IUnknown-Zeiger auf das MSP-Aufrufobjekt zurück.
-   TAPI3 aggregiert das MSP Call-Objekt im TAPI Call-Objekt und macht Schnittstellen wie [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) für die Anwendung verfügbar. Anschließend wird die Anwendung über den neuen Aufruf benachrichtigt.

Die Anwendung kann dann Methoden wie [**ITStream::SelectTerminal verwenden,**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) um die Vorbereitungen für die Anruferledigung abschließen zu können.

## <a name="incoming-call-completion"></a>Abschluss eingehender Aufrufe

-   Die Anwendung ruft [**ITBasicCallControl::Answer auf.**](/windows/win32/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer)
-   TAPI3 ruft [**lineAnswer auf.**](/windows/win32/api/tapi/nf-tapi-lineanswer)
-   TAPISERV ruft [**TSPI \_ lineAnswer auf.**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)
-   Der TSP initiiert das Streaming von Aufrufen. In der Regel sendet der TSP eine Nachricht an den entsprechenden MSP, und der MSP startet die Streams. In einigen TSP/MSP-Implementierungen startet der TSP die Streams.

## <a name="tspmsp-communication-during-call-progress"></a>TSP/MSP-Kommunikation während des Anruffortschritts

Nachdem der Aufruf durchgeführt wurde, kommunizieren der TSP und der MSP, indem sie nicht transparente Puffer über TAPISRV und TAPI3 übergeben.

-   Der TSP sendet Informationen an den MSP, indem er die [**LINE \_ SENDMSPDATA-Nachricht**](line-sendmspdata.md) an TAPISRV sendet.
-   Der MSP empfängt Informationen vom TSP über die [**ITMSPAddress::ReceiveTSPData-Methode.**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-receivetspdata) Wenn die Daten mit einem MSP-Aufrufobjekt verknüpft sind, wird ein Schnittstellenzeiger auf das MSP-Aufrufobjekt als Parameter dieser Methode bereitgestellt.
-   Der MSP sendet Informationen an den TSP, indem er ein \_ MSP-TSP-DATENereignis \_ an TAPI 3 sendet.
-   Der TSP empfängt Informationen vom MSP über die [**\_ TSPI-LineReceiveMSPData-Funktion.**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)

Der genaue Prozess und Inhalt der Kommunikation zwischen Dienstanbietern ist spezifisch für einen bestimmten TSP/MSP-Satz.

> [!Note]  
> Bei ausgehenden Anrufen kennt der MSP in der Regel den Aufruf vor dem TSP. Wenn der MSP versucht, mit dem TSP zu kommunizieren, bevor der TSP über einen Anruf informiert wird, ist die Kommunikation nicht mehr der Reihe. Wenn MSP und TSP Informationen zu einem bestimmten Aufruf austauschen müssen, sollte der TSP die Kommunikation initiieren.

 

 

 
