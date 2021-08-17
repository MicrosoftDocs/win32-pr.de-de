---
title: Messen der Videoqualität
description: Messen der Videoqualität
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capCaptureGetSetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capCaptureSetSetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d3a4d28c12905722447189eabc494b220d737fc0c87f7a9ebc12948390920d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373524"
---
# <a name="measuring-video-quality"></a>Messen der Videoqualität

Eine Möglichkeit zum Messen der Videoqualität besteht darin, die Anzahl der erfassten Frames zu begrenzen, die während des Aufzeichnungsvorgangs gelöscht werden. Wenn die Streamingerfassung abgeschlossen ist, wird der Qualitätswert mit dem Verhältnis von gelöschten Frames zu Gesamtframes verglichen. Wenn der Prozentsatz der gelöschten Frames größer als der Wert des **wPercentDropForError-Members** der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) ist, sendet AVICap bei der Installation eine Fehlermeldung an die Fehlerrückruffunktion.

Sie können den aktuellen Grenzwert für gelöschte Frames (ausgedrückt als Prozentsatz) mithilfe der [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-get-sequence-setup.md) (oder des [**CapCaptureGetSetup-Makros)**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) abrufen. Sie können einen neuen Grenzwert festlegen, indem Sie einen Prozentsatz als Wert des **wPercentDropForError-Members** der **CAPTUREPARMS-Struktur** angeben und dann die aktualisierte Struktur mithilfe der [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-set-sequence-setup.md) (oder des [**CapCaptureSetSetup-Makros)**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) an das Erfassungsfenster senden. Der Standardwert von **wPercentDropForError** ist 10 Prozent.

 

 




