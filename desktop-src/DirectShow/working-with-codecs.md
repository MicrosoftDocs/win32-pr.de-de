---
description: Arbeiten mit Codecs
ms.assetid: c69e0ecf-5f72-4d77-90e6-0f493325c0f4
title: Arbeiten mit Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462a1340ef7e6a64aada586addcc73d95a993884fe2b026e74acde5fd286638c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650619"
---
# <a name="working-with-codecs"></a>Arbeiten mit Codecs

Microsoft Windows stellt mehrere Codecs als Betriebssystemkomponenten bereit. Die verfügbaren Codecs enthalten immer diejenigen, die mit welcher Version von DirectX und Windows Media Player im Windows Release enthalten sind. Zusätzliche Codecs können installiert werden, wenn neuere Versionen von DirectX oder Windows Media Player oder die Windows Media SDK-Runtimes installiert sind. Drittanbieter können zusätzliche Codecs auf einem Hostsystem installieren. Diese Codecs können so entworfen werden, dass sie nur mit einer bestimmten Anwendung funktionieren, oder sie unterstützen die allgemeine Verwendung durch eine directShow-Anwendung.

Codecs können auf eine von drei verschiedenen Arten implementiert werden:

-   Als Video für Windows audio- oder videoinstallierbaren Codec, der vom Videokomprimierungs-Manager (VCM) oder Audiokomprimierungs-Manager (ACM) geladen wird. Im Allgemeinen gilt diese Technologie als veraltet, und ihre Verwendung wird nicht empfohlen. Installierbare Codecs nehmen über den Wrapperfilter AVI Decompressor an DirectShow-Filterdiagrammen teil.
-   Als DirectShow-Filter. Viele Codecs von Drittanbietern werden als native DirectShow-Filter implementiert. Ein solcher Filter ist der Dekomprimiererfilter "Frauen csv MP3". Im Allgemeinen können diese Filter dem Filterdiagramm auf die übliche Weise hinzugefügt werden. Eine Ausnahme von dieser Regel ist, dass einige Windows Media™ Audio- oder Windows Media Video-Codecs und der Microsoft MPEG-4-Codec nicht manuell zu einem Filterdiagramm hinzugefügt werden können. Diese Filter können nur von den FILTERN ASF-Reader und ASF Writer hinzugefügt werden.
-   Als DirectX Media Objects (DMOs). DMOs sind die empfohlene Methode zum Implementieren von Codecs, da sie entweder innerhalb eines DirectShow-Filterdiagramms mithilfe des DMO Wrapperfilters oder unabhängig voneinander in einer anderen Nicht-DirectShow-basierten Streaminganwendung verwendet werden können. Einige Windows Media Audio- und Windows Media Video-Codecs werden als DMOs implementiert. Wie bei den Windows Medienfiltern können diese DMOs nicht außerhalb des Kontexts des Windows Media SDK verwendet werden. Das bedeutet, dass sie in DirectShow nur über den ASF-Reader- oder ASF Writer-Filter zu einem Diagramm hinzugefügt werden können.

In GraphEdit werden alle diese verschiedenen Arten von Codecs in den folgenden Kategorien zusammen angezeigt:

-   Audioaudio
-   Videobeendung
-   DirectShow-Filter

Viele dieser Codecs werden jedoch von Drittanbietern oder von anderen Microsoft-Anwendungen oder Betriebssystemkomponenten installiert und sind nicht für die Verwendung durch andere DirectShow-Anwendungen vorgesehen. Die Liste der in GraphEdit sichtbaren Codecs hängt auch davon ab, welche Version von Windows auf dem Hostsystem ausgeführt wird und welche Version des DirectShow SDK installiert ist.

 

 



