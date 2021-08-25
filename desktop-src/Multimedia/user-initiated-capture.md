---
title: User-Initiated Capture
description: User-Initiated Capture
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Nachricht
- capCaptureGetSetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca015726aabe7c171f37590a98e60774c34a09c219ef445af3e30f199d5030b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892450"
---
# <a name="user-initiated-capture"></a>User-Initiated Capture

Sie können den aktuellen Wert des vom Benutzer initiierten Erfassungsflags abrufen, indem Sie die [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-get-sequence-setup.md) (oder das [**Makro capCaptureGetSetup)**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) verwenden. Der Wert des Flags wird im **fMakeUserHitOKToCapture-Member** der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) gespeichert. Sie können dem Benutzer genau steuern, wann eine Erfassungssitzung gestartet werden soll, indem Sie diesen Member auf **TRUE festlegen.** AVICap zeigt nach dem Zuordnen aller Video- und Audiopuffer für eine Erfassungssitzung ein Dialogfeld an. Dadurch kann der Benutzer Verzögerungen bei der Erfassung aufgrund der Softwarein initialisierung vermeiden. Wenn Ihre Anwendung eine kleine Anzahl von Videopuffern verwendet, ist dieses Dialogfeld wahrscheinlich nicht erforderlich. Der Standardwert ist **FALSE**.

 

 




