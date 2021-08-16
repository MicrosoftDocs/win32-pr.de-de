---
description: Dies ist eine computerspezifische Systemrichtlinie, die verwendet werden kann, wenn der Administrator nur computerspezifische Anwendungen installieren möchte.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 171c003dbe739c890bf15e5c372e40840fee0aabc9159a837c0b5572a8741b76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378513"
---
# <a name="disableuserinstalls"></a>DisableUserInstalls

Dies ist eine computerspezifische [Systemrichtlinie,](system-policy.md) die verwendet werden kann, wenn der Administrator nur computerspezifische Anwendungen installieren möchte.

Wenn diese Richtlinie nicht festgelegt ist, durchsucht das Installationsprogramm die Registrierung nach Anwendungen in der folgenden Reihenfolge: verwaltete Anwendungen, die als benutzerspezifische Anwendungen registriert sind, nicht verwaltete Anwendungen, die als pro Benutzer registriert sind, und schließlich Anwendungen, die pro Computer registriert sind.

Wenn diese Richtlinie auf 1 festgelegt ist, ignoriert das Installationsprogramm alle Als pro Benutzer registrierten Anwendungen und sucht nur nach Anwendungen, die als computerspezifische Anwendungen registriert sind. Aufrufe der Windows Installer-Anwendungsprogrammierschnittstelle oder des Systems ignorieren benutzerspezifische Anwendungen. Wenn versucht wird, eine Installation [](installation-context.md) im Benutzerinstallationskontext durchzuführen, zeigt das Installationsprogramm eine Fehlermeldung an und beendet die Installation. In diesem Fall verhindert der Windows Installer auch benutzerspezifische Installationen von einem Terminalserver.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_** \\ **MACHINE-Softwarerichtlinien** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 



