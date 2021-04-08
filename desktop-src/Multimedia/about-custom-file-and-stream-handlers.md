---
title: Informationen zu benutzerdefinierten Datei-und streamhandlern
description: Informationen zu benutzerdefinierten Datei-und streamhandlern
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
keywords:
- Video für Windows (Vfw), benutzerdefinierte Datei Handler
- Video für Windows (Vfw), benutzerdefinierte Datenstrom Handler
- Video für Windows (Vfw), Datei Handler
- Video für Windows (Vfw), Datenstrom Handler
- VFW (Video für Windows), benutzerdefinierte Datei Handler
- VFW (Video für Windows), benutzerdefinierte Datenstrom Handler
- VFW (Video für Windows), Datei Handler
- VFW (Video für Windows), Datenstrom Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e1872aa8a2f5c55df0db43860e318c792801e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856916"
---
# <a name="about-custom-file-and-stream-handlers"></a>Informationen zu benutzerdefinierten Datei-und streamhandlern

Die Anwendung kann einen benutzerdefinierten Datei Handler zum Lesen aus einer Datei oder schreiben in eine Datei verwenden, die nicht dem Standard entspricht. Zu diesem Zweck verwendet Ihre Anwendung einfach den Namen Ihres Datei Handlers, wenn Sie die Datei öffnen oder die Datei Schnittstelle zuordnen. Die avifile-Bibliothek verwendet dann die Funktionen Ihres Datei Handlers anstelle der von einem anderen Datei Handler. Das nicht dem Standard entsprechende Format wird als Standard-AVI-Daten für Ihre Anwendung oder eine beliebige andere Anwendung mit Ihrem benutzerdefinierten Datei Handler angezeigt.

Ebenso kann die Anwendung einen benutzerdefinierten Datenstrom Handler verwenden, um einen Datenstrom zu lesen, der nicht dem Standard entspricht. Ein Datenstrom – ob es sich um Audiodaten, Video-, MIDI-, Text-oder benutzerdefinierte Daten handelt – ist eine Komponente einer AVI-Datei. Eine AVI-Datei, die eine Videosequenz, einen englischen Sound Sound und einen französischen Sound enthält, besteht beispielsweise aus drei Streams. Die Anwendung kann die Datenströme in einer AVI-Datei angeben, um die Datenströme zu verarbeiten und an einen Handler weiterzuleiten, der den entsprechenden Typ von Multimedia-Daten optimal verarbeiten kann.

> [!Note]  
> Sie müssen benutzerdefinierte Stream-und Datei Handler in einer oder mehreren DLLs platzieren, die von den Haupt Anwendungs Dateien getrennt sind.

 

 

 




