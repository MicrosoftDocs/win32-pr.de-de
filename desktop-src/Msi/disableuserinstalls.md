---
description: Dies ist eine Computer spezifische System Richtlinie, die verwendet werden kann, wenn der Administrator nur Computer spezifische Anwendungen installieren möchte.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: Disableuserinstallationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ee8275567c62fc383c0488d6ad3ef8dfc928f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128392"
---
# <a name="disableuserinstalls"></a>Disableuserinstallationen

Dies ist eine Computer spezifische [System Richtlinie](system-policy.md) , die verwendet werden kann, wenn der Administrator nur Computer spezifische Anwendungen installieren möchte.

Wenn diese Richtlinie nicht festgelegt ist, durchsucht das Installationsprogramm die Registrierung nach Anwendungen in der folgenden Reihenfolge: verwaltete Anwendungen, die als pro Benutzer registrierte, nicht verwaltete Anwendungen registriert sind, und schließlich als pro-Computer registrierte Anwendungen.

Wenn diese Richtlinie auf 1 festgelegt ist, ignoriert das Installationsprogramm alle Anwendungen, die als pro Benutzer registriert sind, und sucht nur nach Anwendungen, die als Computer bezogen registriert sind. Aufrufe an die Windows Installer-Anwendungsprogrammierschnittstelle oder das System ignorieren Anwendungen pro Benutzer. Wenn Sie versuchen, eine Installation im Einzelbenutzer- [Installations Kontext](installation-context.md) auszuführen, zeigt das Installationsprogramm eine Fehlermeldung an und beendet die Installation. In diesem Fall werden durch den Windows Installer auch benutzerspezifische Installationen von einem Terminal Server verhindert.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 



