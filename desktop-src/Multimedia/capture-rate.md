---
title: Erfassungs Rate
description: Erfassungs Rate
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- Captuprojektms-Struktur
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93be9e94f5f9085d25c6ad85a30b115d13349169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036963"
---
# <a name="capture-rate"></a>Erfassungs Rate

Die Erfassungs Rate ist die Anzahl der Frames, die pro Sekunde einer Aufzeichnungs Sitzung aufgezeichnet werden. Sie können die aktuelle Aufzeichnungsrate mithilfe der " [**WM \_ Cap \_ get \_ Sequence \_**](wm-cap-get-sequence-setup.md) "-Setup Nachricht (oder des " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makros) abrufen. Die aktuelle Aufzeichnungsrate wird im **dwrequestmikro secperframe** -Member der [**captuprojektstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur gespeichert. Sie können die Erfassungs Rate festlegen, indem Sie die Anzahl der Mikrosekunden zwischen aufeinander folgenden Frames als Wert dieses Members angeben und dann die aktualisierte **captuprojektstruktur** an das Aufzeichnungs Fenster senden, indem Sie die Setup-Nachricht der [**WM-Cap-Set- \_ \_ \_ Sequenz \_**](wm-cap-set-sequence-setup.md) (oder das [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) -Makro) verwenden. Der Standardwert von **dwrequestmikro secperframe** ist 66667, was 15 Frames pro Sekunde entspricht.

 

 




