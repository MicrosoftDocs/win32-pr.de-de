---
title: Audiopuffer
description: Audiopuffer
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a67f120dc2d2ff956148e5dd4e3992a960641d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709179"
---
# <a name="audio-buffers"></a>Audiopuffer

Sie können den Audioteil eines Aufzeichnungs Vorgangs auf drei Arten steuern:

-   Einschließen oder Ausschließen von Audiodaten aus dem Aufzeichnungs Vorgang.
-   Fordern Sie eine bestimmte Anzahl von audiopuffern an.
-   Fordern Sie an, dass Audiopuffer eine bestimmte Größe aufweisen.

Sie können die Einstellungen für Audiopuffer abrufen, indem Sie [**die \_ \_ get \_ Sequence- \_ Setup**](wm-cap-get-sequence-setup.md) Nachricht (oder das [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) -Makro) der WM-Obergrenze verwenden. Der **fcaptureaudiomember** der [**captumams**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur gibt an, ob Audiodaten in den Aufzeichnungs Vorgang eingeschlossen oder davon ausgeschlossen werden. Die aktuell angeforderte Anzahl der Audiopuffer wird im **wnumaudiorequtzig** -Element gespeichert, und die aktuelle audiopuffergröße wird im **dwaudiobuffersize** -Element gespeichert. Sie können angeben, ob Audioerfassung eingeschlossen werden soll, wie die Größe und Anzahl der Audiopuffer durch Aktualisieren dieser Member angegeben werden soll, und die aktualisierte **captuadapms** -Struktur wird mithilfe der " [**WM \_ Cap \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) "-Setup Nachricht (oder dem [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) -Makro) an das Aufzeichnungs Fenster gesendet.

Standardmäßig ist das Audioformat im Aufzeichnungs Vorgang enthalten, und es werden vier Audiopuffer zugewiesen. Der Standardwert von " **f** " ist " **true**". Die Standardpuffergröße (der Wert von **dwaudiobuffersize**) kann 0,5 Sekunden Audiodaten oder 10K enthalten, je nachdem, welcher Wert größer ist.

 

 




