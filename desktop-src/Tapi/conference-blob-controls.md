---
description: Das folgende Diagramm veranschaulicht die wichtigsten Objekte, die an TAPI 3-Konferenzblobsteuerelementen beteiligt sind. Die angezeigten Schnittstellen werden mit den relevanten Referenzseiten verknüpft.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Konferenzblobsteuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1361951fcb830676e36acb4ec397832629dc5745983c654317a457a0d66ac336
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867992"
---
# <a name="conference-blob-controls"></a>Konferenzblobsteuerelemente

\[Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Das folgende Diagramm veranschaulicht die wichtigsten Objekte, die an TAPI 3-Konferenzblobsteuerelementen beteiligt sind. Die angezeigten Schnittstellen werden mit den relevanten Referenzseiten verknüpft.

![Steuerelemente und Schnittstellen für Konferenzblobs](images/rendblob.png)

Das Konferenzblob enthält anbieterspezifische Informationen zu einem Konferenzobjekt. Ein Zeiger auf das [**ITConferenceBlob-Schnittstellenblob**](itconferenceblob.md) wird durch Ausführen einer QueryInterface für [**ITDirectoryObjectConference ermittelt.**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) Die **ITConferenceBlob-Schnittstelle** stellt Methoden für die grundlegende Bearbeitung eines generischen Konferenzblobs bereit. Eine Anwendung, die Nicht-SDP-Konferenzblobs verwendet, muss eigene Methoden für die Detailbearbeitung implementieren.

Rendezvous stellt die [**ITSdp-Schnittstelle**](itsdp.md) zum Bearbeiten von SDP-Konferenzblobs bereit. Der SDP ist ein Protokoll zum Beschreiben von Multimediasitzungen und deren zugehörigen Planungsinformationen. Weitere Informationen zum SDP-Protokoll finden Sie unter Internet Engineering Task Force (IETF) RFC 2327 mit dem Titel "SDP: Session Description Protocol". Wenn die **ITSDP-Schnittstelle** für ein bestimmtes Konferenzblob vorhanden ist, können Sie einen Zeiger darauf abrufen, indem Sie eine **QueryInterface** für [**ITConferenceBlob ausführen.**](itconferenceblob.md)

Für SDP-Konferenzblobs ermöglichen die [**Schnittstellen ITTimeCollection,**](ittimecollection.md) [**ITTime,**](ittime.md) [**ITMediaCollection**](itmediacollection.md)und [**ITMedia**](itmedia.md) eine detaillierte Steuerung der SDP-Konferenzzeit und der Medienmerkmale.

 

 



