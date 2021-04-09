---
title: Granularität von Video-und audiosegmenten
description: Granularität von Video-und audiosegmenten
ms.assetid: 02c94de7-c7cb-4150-8b3e-0542d317c19b
keywords:
- AVI-Dateien, Segment Granularität
- Avicap-Klasse, Füll Blöcke
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2245b133fbf14bfd6403fa2f3d7e02ed328de6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947831"
---
# <a name="video-and-audio-chunk-granularity"></a>Granularität von Video-und audiosegmenten

Die Segment Granularität ist eine logische Blockgröße für eine AVI-Datei, die zum Schreiben und Abrufen von Audiodaten und Videodaten Segmenten verwendet wird. Beim Schreiben von Audiodaten und Video Blöcken auf den Datenträger fügt avicap bei Bedarf Füll Blöcke (Riff "Junk"-Blöcke) hinzu, um jeden logischen Datenblock auszufüllen.

Sie können die aktuelle Segment granularitätseinstellung mithilfe der " [**WM \_ Cap \_ get \_ Sequence \_**](wm-cap-get-sequence-setup.md) "-Setup Nachricht (oder des " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makros) abrufen. Die aktuelle Segment Granularität wird im **wchunkgranularity** -Member der [**captuprojektstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur gespeichert. Sie können eine neue Segment Granularität als Wert von **wchunkgranularität** angeben und dann die aktualisierte **captuadapms** -Struktur [**mithilfe der**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) Setup-Nachricht der [**WM-Cap- \_ \_ Set- \_ Sequenz \_**](wm-cap-set-sequence-setup.md) an das Aufzeichnungs Fenster senden. Sie können auch NULL für diesen Member angeben, um die Segment Granularität auf die Sektorgröße des Datenträgers festzulegen.

 

 




