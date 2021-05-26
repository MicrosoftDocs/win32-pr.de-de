---
title: Registrierungseintrag zur Laufzeit
description: Registrierungseintrag zur Laufzeit
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player,Laufzeitregistrierungseinträge
- Windows Media Player,Dateierweiterungen
- Windows Media Player,Registrierung
- Registrierung, Dateinamenerweiterungen
- Registrierung, Laufzeiteinträge
- registry,settings for Windows Media Player
- Registrierungseinstellungen der Dateinamenerweiterung
- Laufzeitregistrierungseinträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf485038965184add320e49c29482672c770f48
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424109"
---
# <a name="runtime-registry-entry"></a>Registrierungseintrag zur Laufzeit

Wenn Windows Media Player eine benutzerdefinierte Dateinamenerweiterung findet, sucht sie nach einem Registrierungsunterschlüssel, der der Erweiterung entspricht. Der Unterschlüssel wird unter [File Name Extension Registry Settings (Registrierungseinstellungen für Dateinamenerweiterungen) beschrieben.](file-name-extension-registry-settings.md) Einer der Registrierungseinträge, die unter dem Unterschlüssel der Erweiterung angezeigt werden können, ist der **Runtimeeintrag.**

Der **Eintrag Runtime** gibt die zugrunde liegende Technologie an, die Windows Media Player, um digitale Mediendateien mit der benutzerdefinierten Erweiterung wiedergibt oder zu konvertieren. Der **Eintrag Runtime** hat das folgende Formular.



|   Name   |   Typ         |   Wert                                                       |
|----------|----------------|---------------------------------------------------------------|
| Typ  | **REG \_ DWORD** | Eine positive ganze Zahl, die die zugrunde liegende Technologie identifiziert. |



 

Der Wert des **Runtime-Eintrags** muss einer der folgenden sein.



| **Wert (dezimal)** | **Beschreibung**                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| 6                   | Rendern mit dem Windows Media Format SDK.                                                 |
| 7                   | Rendern mit Microsoft DirectShow.                                                         |
| 13                  | Konvertieren Sie die Datei mithilfe des angegebenen Konvertierungs-Plug-Ins. Erfordert Windows Media Player 11. |



 

Die **Registrierungseintragswerte** 6 und 7 der Runtime werden von Windows Media Player 9er Serie und höher unterstützt. Der Wert 13 wird von Windows Media Player 11 unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ConvertPluginCLSID-Unterschlüssel**](convertpluginclsid-subkey.md)
</dt> <dt>

[**Registrierungseinstellungen für die Dateinamenerweiterung**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




