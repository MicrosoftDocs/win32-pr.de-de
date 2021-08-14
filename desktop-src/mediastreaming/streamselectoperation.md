---
title: StreamSelectOperation-Klasse
description: Registriert einen Ereignishandler, der aufgerufen wird, wenn der von GetMuteAsync gestartete asynchrone Vorgang abgeschlossen wird, und stellt eine Methode zur Rückgabe der Ergebnisse des Vorgangs zur Anwendung. | StreamSelectOperation-Klasse
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- 'StreamSelectOperation-Klasse : Media Streaming-API'
- StreamSelectOperation-Klasse, Media Streaming-API, beschrieben
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161434aad9c4eb20960950ba2dd1979c9caaa2ccc5bbe3c2683ee3e4f839a0b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461560"
---
# <a name="streamselectoperation-class"></a>StreamSelectOperation-Klasse

Registriert einen Ereignishandler, der aufgerufen wird, wenn der von [**GetMuteAsync gestartete asynchrone**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) Vorgang abgeschlossen wird, und stellt eine Methode zur Rückgabe der Ergebnisse des Vorgangs zur Anwendung.

**StreamSelectOperation** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **StreamSelectOperation-Klasse** verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetResults**](streamselectoperation-getresults.md) | Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**SelectBestStreamAsync gestartet wurde.**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **StreamSelectOperation-Klasse** verfügt über diese Eigenschaften.



| Eigenschaft                                                        | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abgeschlossen**](streamselectoperation-completed.md)<br/> | Lesen/Schreiben<br/> | Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest.<br/> |



 

 

