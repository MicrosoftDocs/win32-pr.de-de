---
title: Registrierungs Eintrag für die Laufzeit
description: Registrierungs Eintrag für die Laufzeit
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player, Lauf Zeit Registrierungseinträge
- Windows Media Player, Dateinamen Erweiterungen
- Windows Media Player, Registrierung
- Registrierung, Dateinamen Erweiterungen
- Registrierung, Lauf Zeiteinträge
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Dateinamenerweiterung
- Registrierungseinträge für die Laufzeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01a83c3642f49a9fdbe7f8c51f157a154a9843b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037207"
---
# <a name="runtime-registry-entry"></a>Registrierungs Eintrag für die Laufzeit

Wenn Windows Media Player auf eine benutzerdefinierte Dateierweiterung trifft, sucht es nach einem Registrierungs Unterschlüssel, der der Erweiterung entspricht. Der Unterschlüssel wird in [Registrierungs Einstellungen für Dateinamen Erweiterungen](file-name-extension-registry-settings.md)beschrieben. Einer der Registrierungseinträge, der unter dem Unterschlüssel der Erweiterung angezeigt werden kann, ist der **Lauf** Zeiteintrag.

Der **Lauf** Zeiteintrag gibt die zugrunde liegende Technologie an, mit der Windows Media Player digitale Mediendateien mit der benutzerdefinierten Erweiterung wiedergeben oder konvertieren kann. Der **Lauf** Zeiteintrag weist das folgende Format auf.



|          |                |                                                               |
|----------|----------------|---------------------------------------------------------------|
| **Name** | **Typ**       | **Wert**                                                     |
| Typ  | **REG \_ DWORD** | Eine positive ganze Zahl, die die zugrunde liegende Technologie identifiziert. |



 

Der Wert für den **Lauf** Zeiteintrag muss einer der folgenden Werte sein.



| **Wert (dezimal)** | **Beschreibung**                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| 6                   | Rendering mit dem Windows Media-Format-SDK.                                                 |
| 7                   | Rendering mithilfe von Microsoft DirectShow.                                                         |
| 13                  | Konvertiert die Datei mit dem angegebenen Konvertierungs-Plug-in. Erfordert Windows Media Player 11. |



 

Die **Lauf** Zeit Registrierungs Eintrags Werte 6 und 7 werden von der Windows Media Player 9-Serie und höher unterstützt. Der Wert 13 wird von Windows Media Player 11 unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Convertpluginclsid-Unterschlüssel**](convertpluginclsid-subkey.md)
</dt> <dt>

[**Registrierungs Einstellungen für die Dateinamenerweiterung**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




