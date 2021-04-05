---
title: Indexgröße
description: Indexgröße
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cd9e59c23376a7aa201673ef71743c8a192b60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711585"
---
# <a name="index-size"></a>Indexgröße

Jede AVI-Datei verwendet einen Index einer angegebenen Größe, um Video-und Audiodatenblöcke innerhalb der Datei zu suchen. Ein Eintrag im Index gibt einen Video Frame oder einen Wellenform-Audiopuffer an. Folglich legt der Wert der Indexgröße indirekt die Obergrenze für die Anzahl der Frames fest, die in einer Datei aufgezeichnet werden können.

Sie können die aktuelle Indexgröße abrufen, indem Sie die " [**WM \_ Cap \_ get \_ Sequence \_**](wm-cap-get-sequence-setup.md) "-Setup Nachricht (oder das " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makro) verwenden. Die aktuelle Indexgröße wird im **dwindexsize** -Member der [**captuindems**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur gespeichert. Sie können eine neue Indexgröße als Wert von " **dwindexsize** " angeben und dann die aktualisierte **captuadapms** -Struktur mithilfe der [**\_ \_ \_ \_ Setup**](wm-cap-set-sequence-setup.md) -Nachricht für die WM-Abdeckung (oder dem [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) -Makro) an das Aufzeichnungs Fenster senden. Die Standard Indexgröße beträgt 34.952 Einträge (32-KB-Frames und eine proportionale Anzahl von audiopuffern).

 

 




