---
description: Das Terminal für die Dateiwiedergabe und das Datei Aufzeichnungs Terminal machen die Schnittstellen itterminal und itmultitrackterminal verfügbar. Diese Objekte machen außerdem die itmediacontrol-Schnittstelle verfügbar, die Methoden für das Beenden, starten und die Medien Navigation bereitstellt.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Terminal Dateiwiedergabe Terminal und Datei Aufzeichnungs Terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a73c788e3e1750e44298c1020a088cf8111bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959716"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a>Terminal Dateiwiedergabe Terminal und Datei Aufzeichnungs Terminal

Das Terminal für die Dateiwiedergabe und das Datei Aufzeichnungs Terminal machen die Schnittstellen [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) und [**itmultitrackterminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) verfügbar. Diese Objekte machen außerdem die [**itmediacontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) -Schnittstelle verfügbar, die Methoden für das Beenden, starten und die Medien Navigation bereitstellt.

Das Terminal für die Dateiwiedergabe macht die [**itmediaplayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) -Schnittstelle verfügbar, die über Wiedergabe spezifische Methoden verfügt.

Das Datei Aufzeichnungs Terminal macht die [**itmediarecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) -Schnittstelle verfügbar, die Aufzeichnungs spezifische Methoden bereitstellt.

Bei [Multitrack-Terminals](multitrack-terminals.md)verwalten das Terminal für die Datei Aufzeichnung und das Dateiwiedergabe Terminal jeweils eine Sammlung von nach [Verfolgung von Terminals](track-terminals.md).

 

 
