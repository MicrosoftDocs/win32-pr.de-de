---
title: Videopuffer
description: Videopuffer
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capCaptureGetSetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capCaptureSetSetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a6493d22a495a56084e89d2b067c1cf9a874752b44b81f636b5a184b895199
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687690"
---
# <a name="video-buffers"></a>Videopuffer

Die mit der Videoaufnahme verwendeten Puffer befinden sich im Speicherheap. Die Anzahl von Puffern, die in einem Erfassungsvorgang verwendet werden, kann variieren und hängt vom Wert des **wNumVideoRequested-Elements** der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) und des verfügbaren Systemspeichers ab.

Sie können den aktuellen Wert der angeforderten Videopuffer abrufen, indem Sie die [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-get-sequence-setup.md) (oder das [**CapCaptureGetSetup-Makro)**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) verwenden. Die aktuell angeforderte Anzahl von Videopuffern wird im **wNumVideoRequested-Member** der **CAPTUREPARMS-Struktur** gespeichert. Sie können die Platzierung und Die Anzahl von Puffern anfordern, indem Sie diesen Member aktualisieren und dann die aktualisierte **CAPTUREPARMS-Struktur** mithilfe der [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-set-sequence-setup.md) (oder des [**CapCaptureSetSetup-Makros)**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) an das Erfassungsfenster senden.

 

 




