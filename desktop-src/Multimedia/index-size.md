---
title: Indexgröße
description: Indexgröße
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Nachricht
- capCaptureGetSetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP-Nachricht
- capCaptureSetSetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9742edb1aa73c7b77a56ef3ab2a29a5ea14a1e70351bec1ecb49507bbd0bc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784680"
---
# <a name="index-size"></a>Indexgröße

Jede AVI-Datei verwendet einen Index einer angegebenen Größe, um Video- und Audiodatenbrocken in der Datei zu finden. Ein Eintrag im Index sucht nach einem Videoframe oder Waveform-Audiopuffer. Folglich legt der Wert der Indexgröße indirekt die Obergrenze für die Anzahl von Frames fest, die in einer Datei erfasst werden können.

Sie können die aktuelle Indexgröße mithilfe der [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-get-sequence-setup.md) (oder des [**Makros capCaptureGetSetup)**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) abrufen. Die aktuelle Indexgröße wird im **dwIndexSize-Member** der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) gespeichert. Sie können eine neue Indexgröße als Wert von **dwIndexSize** angeben und dann die aktualisierte **CAPTUREPARMS-Struktur** mithilfe der [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-set-sequence-setup.md) (oder des [**Makros capCaptureSetSetup)**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) an das Erfassungsfenster senden. Die Standardindexgröße beträgt 34.952 Einträge (ermöglicht 32.000 Frames und eine proportionale Anzahl von Audiopuffern).

 

 




