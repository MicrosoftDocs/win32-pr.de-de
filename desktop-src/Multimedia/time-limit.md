---
title: Zeitlimit
description: Zeitlimit
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- CAPTUREPARMS-Struktur
- WM_CAP_GET_SEQUENCE_SETUP-Nachricht
- capCaptureGetSetup-Makro
- CAPTUREPARMS-Struktur
- WM_CAP_SET_SEQUENCE_SETUP-Nachricht
- capCaptureSetSetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b6211edf3ce3fb86b4c0430c685ff05ff7f95c718c0a89e7ba782ae342feb18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801264"
---
# <a name="time-limit"></a>Zeitlimit

Sie können die Dauer eines Erfassungsvorgang begrenzen, indem Sie die **Elemente fLimitEnabled** und **wTimeLimit** der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) verwenden. Der **fLimitEnabled-Member** gibt an, ob der Erfassungsvorgang mit einem Timer durchgeführt werden soll, **während wTimeLimit** die maximale Dauer des Erfassungsvorgang angibt.

Sie können die Werte für **fLimitEnabled** und **wTimeLimit** abrufen, indem Sie die [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-get-sequence-setup.md) (oder das [**Makro capCaptureGetSetup)**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) verwenden. Sie können einen Timer für den Erfassungsvorgang aktivieren, indem Sie **TRUE** als Wert von **fLimitEnabled** angeben, oder Sie können die Dauer des Erfassungsvorgang festlegen, indem Sie einen Wert in Sekunden für **wTimeLimit angeben.** Nachdem Sie diese Member festgelegt haben, senden Sie die aktualisierte [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) mithilfe der [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-set-sequence-setup.md) (oder des [**Makros capCaptureSetSetup)**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) an das Erfassungsfenster. Der Standardwert von **fLimitEnabled ist** **FALSE.**

 

 




