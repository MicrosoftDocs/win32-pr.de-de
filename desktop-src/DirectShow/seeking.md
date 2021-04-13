---
description: Diejenigen
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: Diejenigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef7e82009198a790d5c0f7818599aa13905ce82
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104569255"
---
# <a name="seeking"></a>Diejenigen

Filter unterstützen das Suchen über die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle. Die Anwendung fragt den Filter Graph-Manager nach **imediaseeking** ab und verwendet Sie, um Such Befehle auszugeben. Der Filter Graph-Manager verteilt jeden Seek-Befehl an alle rendererfilter im Diagramm. Jeder Renderer übergibt den Befehls Upstream über die Ausgabe Pins der upstreamfilter, bis er einen Filter erreicht, der die Suche ausführen kann. In der Regel führt ein Quell Filter oder Parserfilter, z. b. der [avi-Splitter](avi-splitter-filter.md), den Suchvorgang aus.

Wenn ein Filter einen Suchvorgang ausführt, werden alle ausstehenden Daten geleert. Das Ergebnis besteht darin, die Latenz von Seek-Befehlen zu minimieren, da vorhandene Daten aus dem Diagramm geleert werden. Nach einem Seek-Befehl wird die streamzeit auf 0 zurückgesetzt.

Das folgende Diagramm veranschaulicht die Abfolge von Ereignissen.

![Abfolge von Ereignissen](images/seeking.png)

Wenn ein Parserfilter über mehr als eine Ausgabe-PIN verfügt, weist er in der Regel einen von Ihnen auf, um Such Befehle zu akzeptieren. Mit den anderen Pins werden alle empfangenen Such Befehle abgelehnt oder ignoriert. Auf diese Weise hält der Parser alle zugehörigen Datenströme synchronisiert. Alle Ausgabe Pins sollten jedoch [**imediaseeking:: getfunktionalitäten**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) und [**imediaseeking:: Check-Funktionen**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) implementieren, um die Suchfunktionen des Filters zurückzugeben. Dadurch wird sichergestellt, dass der Filter Graph-Manager den korrekten Wert an die Anwendung zurückgibt.

Die [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) -Schnittstelle wurde für Filter als veraltet markiert. Automatisierungs Clients müssen diese Schnittstelle weiterhin auf dem Filter Graph-Manager verwenden, da **imediaseeking** nicht Automatisierungs kompatibel ist, aber der Filter Graph-Manager übersetzt alle **imediaposition** -Aufrufe in **imediaseeking** -Aufrufe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lak](flushing.md)
</dt> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



