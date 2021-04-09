---
description: Die Tone-Überwachung überwacht den Mediendaten Strom eines Aufrufes für bestimmte Töne.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Tone-Überwachung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a3275e5207999896792ee04dc1842b01f4ad0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042372"
---
# <a name="tone-monitoring"></a>Tone-Überwachung

Die Tone-Überwachung überwacht den Mediendaten Strom eines Aufrufes für bestimmte Töne. Ein Ton wird durch seine Komponenten Frequenzen und den Rhythmus beschrieben. Durch eine Implementierung der API können mehrere verschiedene Töne gleichzeitig überwacht werden. Eine Anwendung kann jeden Ton markieren, um die verschiedenen Töne zu unterscheiden, für die er eine Erkennung anfordert.

Eine Anwendung kann die Überwachung von Tone für einen angegebenen-Befehl mit [**linemonitortones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)aktivieren bzw. deaktivieren. Mit dieser Funktion gibt die Anwendung an, welche Töne bei einem angegebenen-Befehl erkannt werden sollen. Wenn die Tone-Überwachung aktiviert ist, bewirken erkannte Ziffern, dass die Anwendung mit der [**Zeile \_ monitortone**](line-monitortone.md) -Nachricht benachrichtigt wird. Diese Meldung enthält das Telefon handle, für das der Ton erkannt wurde, sowie das Tag der Anwendung für den Ton.

Der Bereich der Tabellen Überwachung wird durch die Lebensdauer des Aufrufes gebunden. Die Tone-Überwachung bei einem-Rückruf endet, sobald der-Rückruf die Verbindung *trennt oder in* den *Leerlauf* wechselt.

> [!Note]  
> Für die Überwachung von Tönen, Ziffern oder Medientypen ist häufig die Verwendung von Ressourcen erforderlich, von denen der Dienstanbieter nur einen begrenzten Betrag aufweisen kann. Eine Anforderung für die Überwachung kann zurückgewiesen werden, wenn keine Ressourcen verfügbar sind. Aus demselben Grund sollte eine Anwendung jede unnötige Überwachung deaktivieren.

 

 

 



