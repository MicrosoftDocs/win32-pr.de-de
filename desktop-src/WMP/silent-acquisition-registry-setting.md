---
title: Registrierungseinstellung für den automatischen Erwerb
description: Registrierungseinstellung für den automatischen Erwerb
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bdab93c58dd92b5f0522f26ea192150cad4a44ae9a6edfbd0bde770f07a0262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507960"
---
# <a name="silent-acquisition-registry-setting"></a>Registrierungseinstellung für den automatischen Erwerb

Microsoft Windows Media Player verwendet den folgenden Registrierungswert, um zu bestimmen, ob der automatische Erwerb aktiviert werden soll. Dies ist ein Zustand, in dem der Player Nutzungsrechte automatisch herunterlädt, wenn der Benutzer geschützte Inhalte wieder spielt oder synchronisiert.

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **MediaPlayer** \\ **Preferences** \\ **SilentAcquisition**

Der SilentAcquisition-Wert hat das folgende Format:



| Name              | Typ           | Beschreibung                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| SilentAcquisition | **REG \_ DWORD** | Legen Sie diesen Wert auf 1 fest, um den automatischen Erwerb zu aktivieren, oder legen Sie ihn auf 0 fest, um den automatischen Erwerb zu deaktivieren. Der Standardwert ist 1. |



 

Um einen Wert anzugeben, kann der Benutzer Windows Media Player starten, das  Dialogfeld Optionen öffnen, auf die  Registerkarte Datenschutz klicken und dann das Kontrollkästchen Nutzungsrechte automatisch beim Wiederspielen oder Synchronisieren einer Datei herunterladen aktivieren oder löschen.  Wenn Sie dieses Kontrollkästchen aktivieren, wird SilentAcquisition auf 1; Wenn Sie das Kontrollkästchen aktivieren, wird er auf 0 (0) fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungseinstellungen**](registry-settings.md)
</dt> </dl>

 

 




