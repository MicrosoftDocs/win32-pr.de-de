---
title: Verwenden von Ankündigungen
description: Verwenden von Ankündigungen
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Windows Media Metadatei-Wiedergabelisten, Ankündigungen
- Wiedergabelisten, Ankündigungen
- Metadatei-Wiedergabelisten, Ankündigungen
- Windows-Media Player, Ankündigungen
- Ankündigungen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c16fafee1984d08992b96c39d7c3893ea54f682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340825"
---
# <a name="using-announcements"></a>Verwenden von Ankündigungen

Eine Ankündigung ist eine Datei, die Informationen über die URL für einen Medienstrom enthält, einschließlich der Multicast-IP-Adresse, des Ports, des streamformats und anderer Stations Einstellungen. Ankündigungen werden vom Windows Media-Administrator erstellt, wenn ein Unicast-oder Multicast-Veröffentlichungsdaten Strom erstellt wird. Der Client kann die Ankündigungs Datei schnell laden und dann mit dem Zugriff auf die streamingmediendatei fortfahren.

Bei einem unicastpublishing Point wird der Mediendaten Strom des Publishing Points geöffnet. Bei einem Multicast Publishing Point wird die URL aus einer Broadcast Stations Datei mit der Erweiterung. NSC extrahiert, und auf die Streamingmedien wird zugegriffen. Im Gegensatz zu einem unicaststream sind keine Header Informationen in einem Multicast-Stream enthalten. Diese Informationen stammen aus der Broadcast Stations Datei mit der Erweiterung. NSC. Windows Media Player öffnet in der Regel zuerst eine Ankündigungs Datei. Dies ist eine Verwendung für Metadatei-Wiedergabelisten, die auf den Speicherort der Broadcast Stations Datei zeigt.

Beispielcode


```XML
<ASX VERSION="3.0">
    <TITLE>title</TITLE>
    <ENTRY>
        <REF HREF="mms://proseware.com/pubpoint"/>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metafile-Wiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> </dl>

 

 




