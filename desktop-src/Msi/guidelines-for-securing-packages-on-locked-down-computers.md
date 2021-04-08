---
description: Befolgen Sie diese Richtlinien, wenn Sie das Windows Installer Paket erstellen, um eine sichere Software Installation auf gesperrten Computern zu gewährleisten.
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: Sichern von Paketen auf gesperrten Computern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8380ad7e342d35bff80da4d4d86c37759a80a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866315"
---
# <a name="securing-packages-on-locked-down-computers"></a>Sichern von Paketen auf gesperrten Computern

Beachten Sie beim Erstellen eines Windows Installer Pakets, das auf gesperrten Computern verwendet wird, die folgenden Richtlinien, um während der Installation eine sichere Umgebung zu gewährleisten:

-   Testen Sie das Paket auf Kompatibilität mit der Windows Installer Computer- [System Richtlinie](system-policy.md).
-   Stellen Sie sicher, dass das Paket mit allen [Benutzeroberflächen Ebenen](user-interface-levels.md), None, Basic, Limited und Full ausgeführt wird.
-   Testen Sie Ihr Paket auf NTFS-Partitionen, sowohl mit [*erhöhten*](e-gly.md) Berechtigungen als auch mit erhöhten Rechten.
-   Ab Windows Installer 3,0 ermöglicht das [Patchen von Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md) Benutzern, die keine Administratoren sind, das Patchen von Anwendungen, die im computerspezifischen Kontext installiert sind. Testen Sie das Patchpaket unter Windows Vista und Windows XP für die Installation durch Benutzer mit Administrator Zugriff und Benutzer ohne Administratorrechte.

 

 



