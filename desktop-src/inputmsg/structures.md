---
title: Strukturen (Zeiger Eingabe Meldungen und Benachrichtigungen)
description: Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für Zeiger Eingabe Meldungen und Benachrichtigungs Strukturen.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bc796c3924df9a1a349ea2180123f88f56d6a96c
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106365442"
---
# <a name="pointer-input-messages-and-notifications-structures"></a>Zeiger Eingabe Meldungen und Benachrichtigungs Strukturen

Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für [Zeiger Eingabe Meldungen und Benachrichtigungs](messages-and-notifications-portal.md) Strukturen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INPUT_TRANSFORM**](/previous-versions/windows/desktop/api)<br/>                           | Definiert die Matrix, die eine Transformation für einen nachrichtenconsumer darstellt. Diese Matrix kann verwendet werden, um Zeiger Eingabedaten von Client Koordinaten in Bildschirm Koordinaten umzuwandeln, während das Gegenteil zum Transformieren von Zeiger Eingabedaten von Bildschirm Koordinaten in Client Koordinaten verwendet werden kann. <br/>                                                                 |
| [**POINTER_INFO**](/previous-versions/windows/desktop/api)<br/>                          | Enthält grundlegende Zeiger Informationen, die für alle Zeiger Typen gemeinsam sind. Anwendungen können diese Informationen mithilfe der Funktionen [**getpointerinfo**](/previous-versions/windows/desktop/api), [**getpointerframeinfo**](/previous-versions/windows/desktop/api), [**getpointerinfohistory**](/previous-versions/windows/desktop/api) und [**getpointerframeinfohistory**](/previous-versions/windows/desktop/api) abrufen. <br/> |
| [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)<br/>                 | Definiert grundlegende Stift Informationen, die für alle Zeiger Typen gemeinsam sind. <br/>                                                                                                                                                                                                                                                                                                |
| [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api)<br/>             | Definiert grundlegende Berührungs Informationen, die für alle Zeiger Typen gemeinsam sind.<br/>                                                                                                                                                                                                                                                                                               |
| [**Touchvorhertionparameters**](/previous-versions/windows/desktop/api)<br/> | Enthält Details zu Hardware Eingaben, die verwendet werden können, um touchziele vorherzusagen und die Hardware Latenz bei der Verarbeitung von toucheingaben und Gesten Eingaben zu kompensieren, die Entfernungs-und Geschwindigkeitsdaten enthalten.<br/>                                                                                                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verweis auf Zeiger-Eingabe Nachricht](wmpointer-reference.md)
</dt> </dl>

 

 





