---
description: Das folgende Diagramm zeigt die Hauptobjekte, die an den BLOB-Steuerelementen der TAPI 3-Konferenz beteiligt sind Die angezeigten Schnittstellen sind mit den relevanten Referenzseiten hyperverknüpft.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Konferenz-BLOB-Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf13567abd46f56c399cefa732be97b081cfd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527224"
---
# <a name="conference-blob-controls"></a>Konferenz-BLOB-Steuerelemente

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Das folgende Diagramm zeigt die Hauptobjekte, die an den BLOB-Steuerelementen der TAPI 3-Konferenz beteiligt sind Die angezeigten Schnittstellen sind mit den relevanten Referenzseiten hyperverknüpft.

![Conference BLOB-Steuerelemente und-Schnittstellen](images/rendblob.png)

Das Konferenz-BLOB enthält anbieterspezifische Informationen zu einem Konferenz Objekt. Ein Zeiger auf das [**itconferenceblob**](itconferenceblob.md) -Schnittstellen-BLOB wird durch die Durchführung einer QueryInterface-Schnittstelle auf [**itdirectoryobjectconference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)abgerufen. Die **itconferenceblob** -Schnittstelle bietet Methoden für die grundlegende Bearbeitung eines generischen Konferenz-BLOBs. Eine Anwendung, die nicht-SDP-Konferenz-blobvorgänge verwendet, muss für die Detail Bearbeitung eigene Methoden implementieren.

Rendezvous stellt die [**itsdp**](itsdp.md) -Schnittstelle zum Bearbeiten von SDP-Konferenz-blobden bereit. Der SDP ist ein Protokoll zum Beschreiben von Multimedia-Sitzungen und ihrer zugehörigen Zeit Planungsinformationen. Weitere Informationen zum SDP-Protokoll finden Sie unter Internet Engineering Task Force (IETF) RFC 2327 mit dem Titel "SDP: Sitzungs Beschreibungs Protokoll". Wenn die **itsdp** -Schnittstelle für ein bestimmtes Konferenz-BLOB vorhanden ist, können Sie einen Zeiger darauf abrufen, indem Sie eine **QueryInterface** für [**itconferenceblob**](itconferenceblob.md)durchgeführt haben.

Für SDP-Konferenz-blobspeicher ermöglichen die Schnittstellen [**ittimecollection**](ittimecollection.md), [**ittime**](ittime.md), [**itmediacollection**](itmediacollection.md)und [**ITmedia**](itmedia.md) eine ausführliche Steuerung der SDP-Konferenzzeit und der Medien Merkmale.

 

 



