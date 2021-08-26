---
description: Die Tonüberwachung überwacht den Mediendatenstrom eines Aufrufs auf angegebene Töne.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Tonüberwachung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb811d91a70f439ae17123b35967800914bd6a04f1a30168754f602231f038e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034180"
---
# <a name="tone-monitoring"></a>Tonüberwachung

Die Tonüberwachung überwacht den Mediendatenstrom eines Aufrufs auf angegebene Töne. Ein Ton wird durch seine Komponentenhäufigkeiten und den Rhythmus beschrieben. Bei einer Implementierung der API können mehrere unterschiedliche Töne gleichzeitig überwacht werden. Eine Anwendung kann jeden Ton markieren, um die verschiedenen Töne unterscheiden zu können, für die sie eine Erkennung anfordert.

Eine Anwendung kann die Tonüberwachung für einen angegebenen Aufruf mit [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)aktivieren oder deaktivieren. Mit dieser Funktion gibt die Anwendung an, welche Töne bei einem angegebenen Aufruf erkannt werden sollen. Wenn die Tonüberwachung aktiviert ist, bewirken erkannte Ziffern, dass die Anwendung mit der [**LINE \_ MONITORTONE-Meldung**](line-monitortone.md) benachrichtigt wird. Diese Meldung stellt das Aufrufhandle bereit, bei dem der Ton erkannt wurde, sowie das Tag der Anwendung für den Ton.

Der Bereich der Tonüberwachung ist durch die Lebensdauer des Aufrufs gebunden. Die Tonüberwachung für einen Anruf wird beendet, sobald der Anruf *getrennt* wird oder *in den Leerlauf* wechselt.

> [!Note]  
> Die Überwachung von Tönen, Ziffern oder Medientypen erfordert häufig die Verwendung von Ressourcen, deren Größe der Dienstanbieter nur begrenzt haben kann. Eine Anforderung zur Überwachung kann abgelehnt werden, wenn keine Ressourcen verfügbar sind. Aus demselben Grund sollte eine Anwendung jede unnötige Überwachung deaktivieren.

 

 

 



