---
title: User-Initiated Erfassung
description: User-Initiated Erfassung
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856624"
---
# <a name="user-initiated-capture"></a>User-Initiated Erfassung

Sie können den aktuellen Wert des vom Benutzer initiierten Erfassungs Flags abrufen, indem Sie die " [**WM \_ Cap \_ get \_ Sequence \_**](wm-cap-get-sequence-setup.md) "-Setup Nachricht (oder das " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makro) verwenden. Der Wert des Flags wird im **fmakeuserhitektocapture** -Member der [**captuprojektstruktur**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur gespeichert. Sie können dem Benutzer genau steuern, wann eine Aufzeichnungs Sitzung gestartet werden soll, indem Sie dieses Element auf " **true**" festlegen. Avicap zeigt ein Dialogfeld an, nachdem alle Video-und Audiopuffer für eine Aufzeichnungs Sitzung zugeordnet wurden. Dadurch kann der Benutzer aufgrund der Software Initialisierung Aufzeichnungs Verzögerungen vermeiden. Wenn Ihre Anwendung eine kleine Anzahl von Video Puffern verwendet, ist dieses Dialogfeld wahrscheinlich unnötig. Der Standardwert ist **FALSE**.

 

 




