---
description: Installieren Sie ein Windows Installer Paket mit erhöhten Berechtigungen (System).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: Alwaysinstallangehoben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07e705e3e46a28049b6fb85eda96930d645a867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528877"
---
# <a name="alwaysinstallelevated"></a>Alwaysinstallangehoben

Sie können die alwaysinstallerhöhten-Richtlinie verwenden, um ein Windows Installer-Paket mit erhöhten Berechtigungen (System) zu installieren.

* * Warnung: * *

Diese Option entspricht dem erteilen vollständiger Administratorrechte, was ein enormes Sicherheitsrisiko darstellen kann. Microsoft lehnt die Verwendung dieser Einstellung stark ab.

Wenn Sie ein Paket mit erhöhten Berechtigungen (System) installieren möchten, legen Sie den alwaysinstallerhöhten-Wert unter den beiden folgenden Registrierungs Schlüsseln auf "1" fest:

**HKEY \_ Aktuelle \_** Richtlinien für Benutzer \\ **Software** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

Wenn der alwaysinstallerhöhten-Wert unter beiden vorangehenden Registrierungs Schlüsseln nicht auf "1" festgelegt ist, verwendet das Installationsprogramm erweiterte Berechtigungen, um verwaltete Anwendungen zu installieren, und verwendet die Berechtigungsstufe des aktuellen Benutzers für nicht verwaltete Anwendungen.

Da diese Richtlinie es Benutzern ermöglicht, Anwendungen zu installieren, die Zugriff auf Verzeichnisse und Registrierungsschlüssel benötigen, für die der Benutzer möglicherweise nicht über die Berechtigung zum Anzeigen oder ändern verfügt, sollten Sie in Erwägung gezogen werden, ob der Benutzer eine entsprechende Sicherheitsstufe bereitstellt. Durch Festlegen dieser Richtlinie wird Windows Installer angewiesen, System Berechtigungen zu verwenden, wenn die Anwendung auf dem System installiert wird. Wenn diese Richtlinie nicht festgelegt ist, werden Anwendungen, die nicht vom Administrator verteilt werden, mit den Berechtigungen des Benutzers installiert, und nur verwaltete Anwendungen erhalten erhöhte Rechte.

Beachten Sie, dass jeder Benutzer seine Einstellung pro Benutzer festlegen kann, sobald die Computer spezifische Richtlinie für alwaysinstallerhöhten aktiviert ist.

## <a name="remarks"></a>Bemerkungen

Informationen zur Interaktion dieser Richtlinie mit Installations Quellen finden Sie unter [Verwalten von Installations Quellen](managing-installation-sources.md).

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 



