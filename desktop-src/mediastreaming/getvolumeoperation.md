---
title: Getvolumeoperation-Klasse
description: Registriert einen Ereignishandler, der aufgerufen wird, wenn der von getvolumeasync gestartete asynchrone Vorgang abgeschlossen ist, und stellt eine Methode bereit, die die Ergebnisse des Vorgangs zurückgibt.
ms.assetid: F7BCE2AB-89B5-44CE-8BDF-347F2E3FD6C9
keywords:
- Getvolumeoperation-Klasse Medien Streaming-API
- Getvolumeoperation-Klasse Medien Streaming-API, beschrieben
topic_type:
- apiref
api_name:
- GetVolumeOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ac06bfb85e8ebbf10306da43cb44c7e3b3e862a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340703"
---
# <a name="getvolumeoperation-class"></a>Getvolumeoperation-Klasse

Registriert einen Ereignishandler, der aufgerufen wird, wenn der von [**getvolumeasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) gestartete asynchrone Vorgang abgeschlossen ist, und stellt eine Methode bereit, die die Ergebnisse des Vorgangs zurückgibt.

**Getvolumeoperation** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **getvolumeoperation** -Klasse verfügt über diese Methoden.



| Methode                                              | BESCHREIBUNG                                                                                                                      |
|:----------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**GetResults**](getvolumeoperation-getresults.md) | Gibt die Ergebnisse des asynchronen Vorgangs zurück, der von [**getvolumeasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync)gestartet wurde.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **getvolumeoperation** -Klasse verfügt über diese Eigenschaften.



| Eigenschaft                                                     | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abgeschlossen**](getvolumeoperation-completed.md)<br/> | Lesen/Schreiben<br/> | Ruft einen Ereignishandler ab, der aufgerufen wird, wenn der von [**getvolumeasync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) gestartete asynchrone Vorgang abgeschlossen ist, oder legt diesen fest. <br/> |



 

 

