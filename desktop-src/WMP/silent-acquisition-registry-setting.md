---
title: Registrierungs Einstellung für automatische Übernahme
description: Registrierungs Einstellung für automatische Übernahme
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a00bbb6d930cb137ed12ffbcb05af31cee3c99c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341872"
---
# <a name="silent-acquisition-registry-setting"></a>Registrierungs Einstellung für automatische Übernahme

Microsoft Windows Media Player verwendet den folgenden Registrierungs Wert, um zu bestimmen, ob die automatische Übernahme aktiviert werden soll, einen Status, in dem der Player die Nutzungsrechte automatisch herunterlädt, wenn der Benutzer geschützte Inhalte wieder gibt oder synchronisiert.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Media Player** \\ **Preferences** \\ **silenterwerbs**

Der silenterwerbs-Wert weist die folgende Form auf:



| Name              | type           | BESCHREIBUNG                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| Silenterwerbs | **REG \_ DWORD** | Legen Sie diesen Wert auf 1 fest, um die automatische Erfassung zu aktivieren, oder auf 0, um die automatische Erfassung zu deaktivieren. Der Standardwert ist 1. |



 

Um einen Wert anzugeben, kann der Benutzer Windows Media Player starten, das Dialogfeld **Optionen** öffnen, auf die Registerkarte **Datenschutz** klicken und dann das Kontrollkästchen **Nutzungsrechte automatisch beim wiedergeben oder Synchronisieren einer Datei herunterladen** deaktivieren bzw. deaktivieren. Wenn Sie dieses Kontrollkästchen aktivieren, wird silentacquisition auf 1 festgelegt. Wenn Sie das Kontrollkästchen deaktivieren, wird es auf 0 festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungs Einstellungen**](registry-settings.md)
</dt> </dl>

 

 




