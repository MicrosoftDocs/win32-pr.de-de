---
description: Das Terminal für die Dateiwiedergabe und das Dateiaufzeichnungsterminal machen die Schnittstellen ITTerminal und ITMultiTrackTerminal verfügbar. Diese Objekte machen auch die ITMediaControl-Schnittstelle verfügbar, die Methoden zum Beenden, Starten und Navigieren von Medien bietet.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Terminal für Dateiwiedergabe und Dateiaufzeichnungsterminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad07ea46e2abf13465ac3344e69f586673c3b29463eac8bdd324966fb838368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100590"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a>Terminal für Dateiwiedergabe und Dateiaufzeichnungsterminal

Das Terminal für die Dateiwiedergabe und das Dateiaufzeichnungsterminal machen die [**Schnittstellen ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) und [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) verfügbar. Diese Objekte machen auch die [**ITMediaControl-Schnittstelle**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) verfügbar, die Methoden zum Beenden, Starten und Navigieren von Medien bietet.

Das Terminal für die Dateiwiedergabe macht die [**ITMediaPlayback-Schnittstelle**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) verfügbar, die über wiedergabespezifische Methoden verfügt.

Das Terminal für die Dateiaufzeichnung macht die [**ITMediaRecord-Schnittstelle**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) verfügbar, die aufzeichnungsspezifische Methoden bietet.

Als [Multitrack-Terminals](multitrack-terminals.md)verwalten das Terminal für die Dateiaufzeichnung und das Dateiwiedergabeterminal jeweils eine Sammlung von [Trackterminals.](track-terminals.md)

 

 
