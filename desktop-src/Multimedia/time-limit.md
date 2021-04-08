---
title: Zeitlimit
description: Zeitlimit
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- Captuprojektms-Struktur
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- Captuprojektms-Struktur
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878c76ab1e380fe878cd8c9493163bcb71e574cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714441"
---
# <a name="time-limit"></a>Zeitlimit

Sie können die Dauer eines Aufzeichnungs Vorgangs beschränken, indem Sie die Elemente **flimitenabled** und **wtimelimit** der [**captuvertrams**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur verwenden. Der **flimitenabled** -Member gibt an, ob der Aufzeichnungs Vorgang zeitgleich ist, während **wtimelimit** die maximale Dauer des Aufzeichnungs Vorgangs angibt.

Sie können die Werte für " **flimitenabled** " und " **wtimelimit** " mithilfe der " [**WM \_ Cap \_ get \_ Sequence \_**](wm-cap-get-sequence-setup.md) "-Setup Nachricht (oder des " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makros) abrufen. Sie können einen Timer für den Aufzeichnungs Vorgang aktivieren, indem Sie " **true** " als Wert von " **flimitenabled**" angeben, oder Sie können die Dauer des Aufzeichnungs Vorgangs festlegen, indem Sie einen Wert (in Sekunden) für " **wtimelimit**" angeben. Nachdem Sie diese Member festgelegt haben, senden Sie die aktualisierte [**captuadapms**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur mithilfe der " [**WM \_ Cap \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) "-Setup Nachricht (oder dem " [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) "-Makro) an das Aufzeichnungs Fenster. Der Standardwert von **flimitenabled** ist **false**.

 

 




