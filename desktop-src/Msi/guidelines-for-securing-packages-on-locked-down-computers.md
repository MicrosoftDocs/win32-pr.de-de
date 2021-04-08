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
# <a name="securing-packages-on-locked-down-computers"></a><span data-ttu-id="72e5c-103">Sichern von Paketen auf gesperrten Computern</span><span class="sxs-lookup"><span data-stu-id="72e5c-103">Securing Packages on Locked-Down Computers</span></span>

<span data-ttu-id="72e5c-104">Beachten Sie beim Erstellen eines Windows Installer Pakets, das auf gesperrten Computern verwendet wird, die folgenden Richtlinien, um während der Installation eine sichere Umgebung zu gewährleisten:</span><span class="sxs-lookup"><span data-stu-id="72e5c-104">Adherence to the following guidelines when authoring a Windows Installer package that will be used on locked-down computers helps maintain a secure environment during installation:</span></span>

-   <span data-ttu-id="72e5c-105">Testen Sie das Paket auf Kompatibilität mit der Windows Installer Computer- [System Richtlinie](system-policy.md).</span><span class="sxs-lookup"><span data-stu-id="72e5c-105">Test your package for compatibility with the Windows Installer machine [System Policy](system-policy.md).</span></span>
-   <span data-ttu-id="72e5c-106">Stellen Sie sicher, dass das Paket mit allen [Benutzeroberflächen Ebenen](user-interface-levels.md), None, Basic, Limited und Full ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72e5c-106">Make sure you package runs with all [user interface levels](user-interface-levels.md), none, basic, limited, and full.</span></span>
-   <span data-ttu-id="72e5c-107">Testen Sie Ihr Paket auf NTFS-Partitionen, sowohl mit [*erhöhten*](e-gly.md) Berechtigungen als auch mit erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="72e5c-107">Test your package on NTFS partitions, both with [*elevated*](e-gly.md) and non-elevated privileges.</span></span>
-   <span data-ttu-id="72e5c-108">Ab Windows Installer 3,0 ermöglicht das [Patchen von Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md) Benutzern, die keine Administratoren sind, das Patchen von Anwendungen, die im computerspezifischen Kontext installiert sind.</span><span class="sxs-lookup"><span data-stu-id="72e5c-108">Starting with Windows Installer 3.0, [User Account Control (UAC) Patching](user-account-control--uac--patching.md) enables non-administrator users to patch applications installed in the per-machine context.</span></span> <span data-ttu-id="72e5c-109">Testen Sie das Patchpaket unter Windows Vista und Windows XP für die Installation durch Benutzer mit Administrator Zugriff und Benutzer ohne Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="72e5c-109">Test your patch package on Windows Vista and Windows XP for both installation by users with administrator access and by non-administrator users.</span></span>

 

 



