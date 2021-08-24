---
title: Erfassungsrate
description: Erfassungsrate
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capCaptureGetSetup-Makro
- CAPTUREPARMS-Struktur
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capCaptureSetSetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855cff56e36d9a246e1f18ae5fc4e3c09a200a2114104424f053a8780881de93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691660"
---
# <a name="capture-rate"></a>Erfassungsrate

Die Erfassungsrate ist die Anzahl der Frames, die jede Sekunde einer Erfassungssitzung erfasst werden. Sie können die aktuelle Erfassungsrate abrufen, indem Sie die [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-get-sequence-setup.md) (oder das [**CapCaptureGetSetup-Makro)**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) verwenden. Die aktuelle Erfassungsrate wird im **dwRequestMicroSecPerFrame-Member** der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) gespeichert. Sie können die Erfassungsrate festlegen, indem Sie die Anzahl der Mikrosekunden zwischen aufeinander folgenden Frames als Wert dieses Members angeben und dann die aktualisierte **CAPTUREPARMS-Struktur** mithilfe der [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-set-sequence-setup.md) (oder des [**CapCaptureSetSetup-Makros)**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) an das Erfassungsfenster senden. Der Standardwert von **dwRequestMicroSecPerFrame** ist 66667, was 15 Frames pro Sekunde entspricht.

 

 




