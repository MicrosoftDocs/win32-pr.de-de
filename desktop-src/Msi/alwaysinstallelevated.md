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
# <a name="alwaysinstallelevated"></a><span data-ttu-id="f7791-103">Alwaysinstallangehoben</span><span class="sxs-lookup"><span data-stu-id="f7791-103">AlwaysInstallElevated</span></span>

<span data-ttu-id="f7791-104">Sie können die alwaysinstallerhöhten-Richtlinie verwenden, um ein Windows Installer-Paket mit erhöhten Berechtigungen (System) zu installieren.</span><span class="sxs-lookup"><span data-stu-id="f7791-104">You can use the AlwaysInstallElevated policy to install a Windows Installer package with elevated (system) privileges.</span></span>

<span data-ttu-id="f7791-105">\* \* Warnung: \* \*</span><span class="sxs-lookup"><span data-stu-id="f7791-105">\*\*Warning:  \*\*</span></span>

<span data-ttu-id="f7791-106">Diese Option entspricht dem erteilen vollständiger Administratorrechte, was ein enormes Sicherheitsrisiko darstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f7791-106">This option is equivalent to granting full administrative rights, which can pose a massive security risk.</span></span> <span data-ttu-id="f7791-107">Microsoft lehnt die Verwendung dieser Einstellung stark ab.</span><span class="sxs-lookup"><span data-stu-id="f7791-107">Microsoft strongly discourages the use of this setting.</span></span>

<span data-ttu-id="f7791-108">Wenn Sie ein Paket mit erhöhten Berechtigungen (System) installieren möchten, legen Sie den alwaysinstallerhöhten-Wert unter den beiden folgenden Registrierungs Schlüsseln auf "1" fest:</span><span class="sxs-lookup"><span data-stu-id="f7791-108">To install a package with elevated (system) privileges, set the AlwaysInstallElevated value to "1" under both of the following registry keys:</span></span>

<span data-ttu-id="f7791-109">**HKEY \_ Aktuelle \_** Richtlinien für Benutzer \\ **Software** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="f7791-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="f7791-110">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="f7791-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="f7791-111">Wenn der alwaysinstallerhöhten-Wert unter beiden vorangehenden Registrierungs Schlüsseln nicht auf "1" festgelegt ist, verwendet das Installationsprogramm erweiterte Berechtigungen, um verwaltete Anwendungen zu installieren, und verwendet die Berechtigungsstufe des aktuellen Benutzers für nicht verwaltete Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="f7791-111">If the AlwaysInstallElevated value is not set to "1" under both of the preceding registry keys, the installer uses elevated privileges to install managed applications and uses the current user's privilege level for unmanaged applications.</span></span>

<span data-ttu-id="f7791-112">Da diese Richtlinie es Benutzern ermöglicht, Anwendungen zu installieren, die Zugriff auf Verzeichnisse und Registrierungsschlüssel benötigen, für die der Benutzer möglicherweise nicht über die Berechtigung zum Anzeigen oder ändern verfügt, sollten Sie in Erwägung gezogen werden, ob der Benutzer eine entsprechende Sicherheitsstufe bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f7791-112">Because this policy permits users to install applications that require access to directories and registry keys for which the user may not have permission to view or change, you should consider whether it provides your users with an appropriate level of security.</span></span> <span data-ttu-id="f7791-113">Durch Festlegen dieser Richtlinie wird Windows Installer angewiesen, System Berechtigungen zu verwenden, wenn die Anwendung auf dem System installiert wird.</span><span class="sxs-lookup"><span data-stu-id="f7791-113">Setting this policy directs Windows Installer to use system permissions when it installs the application on the system.</span></span> <span data-ttu-id="f7791-114">Wenn diese Richtlinie nicht festgelegt ist, werden Anwendungen, die nicht vom Administrator verteilt werden, mit den Berechtigungen des Benutzers installiert, und nur verwaltete Anwendungen erhalten erhöhte Rechte.</span><span class="sxs-lookup"><span data-stu-id="f7791-114">If this policy is not set, applications not distributed by the administrator are installed using the user's privileges and only managed applications get elevated privileges.</span></span>

<span data-ttu-id="f7791-115">Beachten Sie, dass jeder Benutzer seine Einstellung pro Benutzer festlegen kann, sobald die Computer spezifische Richtlinie für alwaysinstallerhöhten aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f7791-115">Note that once the per-machine policy for AlwaysInstallElevated is enabled, any user can set their per-user setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7791-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7791-116">Remarks</span></span>

<span data-ttu-id="f7791-117">Informationen zur Interaktion dieser Richtlinie mit Installations Quellen finden Sie unter [Verwalten von Installations Quellen](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="f7791-117">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="f7791-118">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f7791-118">Data Type</span></span>

<span data-ttu-id="f7791-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f7791-119">**REG\_DWORD**</span></span>

 

 



