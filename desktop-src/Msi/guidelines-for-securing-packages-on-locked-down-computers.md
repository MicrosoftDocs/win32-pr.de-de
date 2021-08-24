---
description: Um eine sichere Softwareinstallation auf gesperrten Computern zu gewährleisten, befolgen Sie diese Richtlinien beim Erstellen des Windows Installer-Pakets.
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: Sichern von Paketen auf gesperrten Computern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bcdb2770e165a8b0d99fbc2088ec4c3b113e5befa180a7d6d2598eee866a5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315300"
---
# <a name="securing-packages-on-locked-down-computers"></a>Sichern von Paketen auf gesperrten Computern

Die Einhaltung der folgenden Richtlinien beim Erstellen eines Windows Installer-Pakets, das auf gesperrten Computern verwendet wird, trägt zur Aufrechterhaltung einer sicheren Umgebung während der Installation bei:

-   Testen Sie Ihr Paket auf Kompatibilität mit der [Systemrichtlinie](system-policy.md)des Windows Installer-Computers.
-   Stellen Sie sicher, dass das Paket mit allen [Benutzeroberflächenebenen](user-interface-levels.md), none, basic, limited und full ausgeführt wird.
-   Testen Sie Ihr Paket auf NTFS-Partitionen mit [*erhöhten*](e-gly.md) und nicht erhöhten Rechten.
-   Ab Windows Installer 3.0 ermöglicht das Patchen der [Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md) Benutzern ohne Administratorrechte das Patchen von Anwendungen, die im Kontext pro Computer installiert sind. Testen Sie Ihr Patchpaket auf Windows Vista und Windows XP sowohl für die Installation durch Benutzer mit Administratorzugriff als auch für Benutzer ohne Administratorrechte.

 

 



