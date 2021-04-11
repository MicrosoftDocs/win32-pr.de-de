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
# <a name="disableuserinstalls"></a><span data-ttu-id="0dbf2-103">Disableuserinstallationen</span><span class="sxs-lookup"><span data-stu-id="0dbf2-103">DisableUserInstalls</span></span>

<span data-ttu-id="0dbf2-104">Dies ist eine Computer spezifische [System Richtlinie](system-policy.md) , die verwendet werden kann, wenn der Administrator nur Computer spezifische Anwendungen installieren möchte.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-104">This is a per-machine [system policy](system-policy.md) that can be used when the administrator only wants per-machine applications installed.</span></span>

<span data-ttu-id="0dbf2-105">Wenn diese Richtlinie nicht festgelegt ist, durchsucht das Installationsprogramm die Registrierung nach Anwendungen in der folgenden Reihenfolge: verwaltete Anwendungen, die als pro Benutzer registrierte, nicht verwaltete Anwendungen registriert sind, und schließlich als pro-Computer registrierte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-105">If this policy is not set, the installer searches the registry for applications in the following order: managed applications registered as per-user, unmanaged applications registered as per-user, and finally applications registered as per-machine.</span></span>

<span data-ttu-id="0dbf2-106">Wenn diese Richtlinie auf 1 festgelegt ist, ignoriert das Installationsprogramm alle Anwendungen, die als pro Benutzer registriert sind, und sucht nur nach Anwendungen, die als Computer bezogen registriert sind.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-106">If this policy is set to 1, the installer ignores all applications registered as per-user and only searches for applications registered as per-machine.</span></span> <span data-ttu-id="0dbf2-107">Aufrufe an die Windows Installer-Anwendungsprogrammierschnittstelle oder das System ignorieren Anwendungen pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-107">Calls to the Windows Installer application programming interface or system ignore per-user applications.</span></span> <span data-ttu-id="0dbf2-108">Wenn Sie versuchen, eine Installation im Einzelbenutzer- [Installations Kontext](installation-context.md) auszuführen, zeigt das Installationsprogramm eine Fehlermeldung an und beendet die Installation.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-108">An attempt to perform an installation in the per-user [installation context](installation-context.md) causes the installer to display an error message and stops the installation.</span></span> <span data-ttu-id="0dbf2-109">In diesem Fall werden durch den Windows Installer auch benutzerspezifische Installationen von einem Terminal Server verhindert.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-109">In this case, the Windows Installer also prevents per-user installations from a terminal server.</span></span>

## <a name="registry-key"></a><span data-ttu-id="0dbf2-110">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="0dbf2-110">Registry Key</span></span>

<span data-ttu-id="0dbf2-111">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="0dbf2-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="0dbf2-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0dbf2-112">Data Type</span></span>

<span data-ttu-id="0dbf2-113">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0dbf2-113">**REG\_DWORD**</span></span>

 

 



