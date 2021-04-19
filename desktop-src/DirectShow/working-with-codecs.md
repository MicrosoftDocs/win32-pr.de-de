---
description: Arbeiten mit Codecs
ms.assetid: c69e0ecf-5f72-4d77-90e6-0f493325c0f4
title: Arbeiten mit Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe6d45608c3d95fee8f67344bdec0fc77431919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347027"
---
# <a name="working-with-codecs"></a>Arbeiten mit Codecs

Microsoft Windows bietet mehrere Codecs als Betriebssystemkomponenten. Die verfügbaren Codecs enthalten immer diejenigen, die mit der Version von DirectX und Windows Media Player ausgeliefert wurden, die in der Windows-Version enthalten war. Weitere Codecs können installiert werden, wenn neuere Versionen von DirectX oder Windows Media Player oder Windows Media SDK-Laufzeiten installiert sind. Drittanbieter können zusätzliche Codecs auf einem Host System installieren. Diese Codecs können so entworfen werden, dass Sie nur mit einer bestimmten Anwendung funktionieren, oder Sie unterstützen möglicherweise die allgemeine Verwendung durch eine beliebige DirectShow-Anwendung.

Codecs können auf drei verschiedene Arten implementiert werden:

-   Ein Video für den Windows-Typ-Audiotyp oder den Video installierbaren Codec, der vom Videokomprimierungs-Manager (VCM) oder vom Audiokomprimierungs-Manager (ACM) geladen wird. Im Allgemeinen gilt diese Technologie als veraltet und wird nicht empfohlen. Installierbare Codecs sind an DirectShow-Filter Diagrammen über den AVI-Debug-Wrapper Filter beteiligt.
-   Als DirectShow-Filter. Viele Codecs von Drittanbietern werden als Native DirectShow-Filter implementiert. Ein solcher Filter ist der "Frauenhofer MP3-Debug-Filter". Im Allgemeinen können diese Filter auf die übliche Weise dem Filter Diagramm hinzugefügt werden. Eine Ausnahme von dieser Regel besteht darin, dass einige Windows Media™-Audiodaten oder-Windows Media Video Codecs und der Microsoft MPEG-4-Codec nicht manuell zu einem Filter Diagramm hinzugefügt werden können. Diese Filter können nur von den "ASF Reader"-und "ASF Writer"-Filtern hinzugefügt werden.
-   Als DirectX Media Objects (DMOs). DMOS sind die empfohlene Methode zum Implementieren von Codecs, da Sie entweder innerhalb eines DirectShow-Filter Diagramms mithilfe des DMO-Wrapper Filters oder anderweitig in jeder anderen nicht-DirectShow-basierten Streaminganwendung verwendet werden können. Einige Windows Media Audio und Windows Media Video Codecs werden als DMOS implementiert. Wie bei den Windows Media-filtern können diese DMOS nicht außerhalb des Kontexts des Windows Media SDK verwendet werden. Dies bedeutet, dass Sie in DirectShow nur über die Funktionen des ASF-Readers oder des ASF-Writers einem Diagramm hinzugefügt werden können.

In GraphEdit werden alle diese unterschiedlichen Arten von Codecs in den folgenden Kategorien angezeigt:

-   Audiokompressor
-   Video-Kompressor
-   DirectShow-Filter

Viele dieser Codecs werden jedoch von Drittanbietern oder von anderen Microsoft-Anwendungen oder-Betriebssystemkomponenten installiert und sind nicht für die Verwendung durch andere DirectShow-Anwendungen vorgesehen. Die Liste der in GraphEdit sichtbaren Codecs hängt auch davon ab, welche Version von Windows auf dem Host System ausgeführt wird und welche Version des DirectShow SDK installiert ist.

 

 



