---
title: Verwenden von Ankündigungen
description: Verwenden von Ankündigungen
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Windows Wiedergabelisten von Medienmetadateien,Ankündigungen
- Wiedergabelisten,Ankündigungen
- Metafile-Wiedergabelisten,Ankündigungen
- Windows Media Player,Ankündigungen
- Ankündigungen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 24408211f6ce708d380406026de45be0cce86521fdc188aaaf785ccf03790c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134383"
---
# <a name="using-announcements"></a>Verwenden von Ankündigungen

Eine Ankündigung ist eine Datei, die Informationen zur URL für einen Medienstream enthält, einschließlich der Multicast-IP-Adresse, des Ports, des Streamformats und anderer Stationseinstellungen. Ankündigungen werden von einem Windows erstellt, wenn ein Unicast- oder Multicastveröffentlichungsstream erstellt wird. Der Client kann die Ankündigungsdatei schnell laden und dann mit dem Zugriff auf die Streamingmediendatei fortfahren.

Bei einem Unicastveröffentlichungspunkt wird der Medienstream des Veröffentlichungspunkts geöffnet. Bei einem Multicastveröffentlichungspunkt wird die URL aus einer Broadcaststationsdatei mit der Erweiterung .nsc extrahiert, und auf das Streamingmedium wird zugegriffen. Im Gegensatz zu einem Unicaststream sind keine Headerinformationen in einem Multicaststream enthalten. Diese Informationen stammen aus der Broadcaststationsdatei mit der Erweiterung .nsc. Windows Media Player öffnet in der Regel zuerst eine Ankündigungsdatei. Dies ist eine Verwendung für Metadateiwiedergabelisten, die auf den Speicherort der Broadcaststationsdatei verweist.

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

[**Erstellen von Metadateiwiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> </dl>

 

 




