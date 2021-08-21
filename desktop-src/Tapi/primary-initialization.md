---
description: Eine TAPI-Anwendung muss einen Initialisierungsvorgang aufrufen, bei dem eine Reihe von Aktionen von TAPI und den Dienstanbietern, die die Kommunikationsumgebung für die Anwendung eingerichtet haben, aufgefordert wird.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Primäre Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae187692f1eb64546398a273bc823ab93f622b6a0472848c31f9d94b9ecd7e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060588"
---
# <a name="primary-initialization"></a>Primäre Initialisierung

Eine TAPI-Anwendung muss einen Initialisierungsvorgang aufrufen, bei dem eine Reihe von Aktionen von TAPI und den Dienstanbietern, die die Kommunikationsumgebung für die Anwendung eingerichtet haben, aufgefordert wird.

-   Die Initialisierung ist synchron und gibt erst dann zurück, wenn der Vorgang abgeschlossen ist oder fehlgeschlagen ist.
-   Wenn TAPISRV noch nicht ausgeführt wird, wird es von TAPI gestartet.
-   TAPI richtet eine Verbindung mit dem TAPISRV-Prozess ein.
-   TAPISVR lädt die in der Registrierung angegebenen Dienstanbieter und fordert sie auf, die unterstützten Geräte zu initialisieren.

**TAPI 2.x:** Anwendungen führen die Initialisierung durch Aufrufen [**von lineInitializeEx aus.**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)

**TAPI 3.x:** Anwendungen rufen [**ITTAPI::Initialize auf.**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)

 

 
