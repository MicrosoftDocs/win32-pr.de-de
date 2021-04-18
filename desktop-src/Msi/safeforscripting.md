---
description: Wenn diese pro-Computer-System Richtlinie auf &\# 0034; 1&0034; festgelegt ist \# , werden Benutzer vom Installationsprogramm nicht aufgefordert, wenn Skripts in einer Webseite die Automatisierungsschnittstelle des Installers verwenden.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: Safeforscripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2907c4b021101ff936bdddf98a5cc1e32a01b991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354591"
---
# <a name="safeforscripting"></a><span data-ttu-id="334ab-103">Safeforscripting</span><span class="sxs-lookup"><span data-stu-id="334ab-103">SafeForScripting</span></span>

<span data-ttu-id="334ab-104">Wenn diese pro-Computer- [System Richtlinie](system-policy.md) auf "1" festgelegt ist, werden Benutzer vom Installationsprogramm nicht aufgefordert, wenn Skripts innerhalb einer Webseite die [Automatisierungsschnittstelle](automation-interface.md)des Installers verwenden.</span><span class="sxs-lookup"><span data-stu-id="334ab-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer does not prompt users when scripts within a Web page use the installer's [automation interface](automation-interface.md).</span></span>

<span data-ttu-id="334ab-105">Vor dem Festlegen dieser Richtlinie sollten Sie in Erwägung gezogen werden, ob die Benutzer Aufforderung eine entsprechende Sicherheitsstufe für Ihre Benutzer bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="334ab-105">Before setting this policy, you should consider whether foregoing the user prompt provides an appropriate level of security for your users.</span></span> <span data-ttu-id="334ab-106">Wenn diese Richtlinie nicht festgelegt ist und ein von einem Internet Browser gehosteter Skript versucht, eine Anwendung zu installieren, warnt das System den Benutzer und fordert Sie auf, die Installation zu akzeptieren oder abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="334ab-106">If this policy is not set, when a script hosted by an Internet browser tries to install an application, the system warns the user and asks them to accept or refuse the installation.</span></span> <span data-ttu-id="334ab-107">Durch das Festlegen von safeforscripting wird diese Warnung unterdrückt, und die Installation von Anwendungen auf dem System kann ohne das Wissen des Benutzers zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="334ab-107">Setting SafeForScripting suppresses this warning and may allow the installation of applications on the system without the user's knowledge.</span></span> <span data-ttu-id="334ab-108">Diese Richtlinie kann für ein Unternehmen nützlich sein, das webbasierte Tools zum Verteilen von Programmen verwendet.</span><span class="sxs-lookup"><span data-stu-id="334ab-108">This policy may be useful for an enterprise that uses web-based tools to distribute programs.</span></span>

<span data-ttu-id="334ab-109">Weitere Informationen finden Sie unter [Richtlinien zum Erstellen sicherer Installationen](guidelines-for-authoring-secure-installations.md) und [digitaler Signaturen und Windows Installer](digital-signatures-and-windows-installer.md) und [Herunterladen einer-Installation aus dem Internet](downloading-an-installation-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="334ab-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="334ab-110">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="334ab-110">Registry Key</span></span>

<span data-ttu-id="334ab-111">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="334ab-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="334ab-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="334ab-112">Data Type</span></span>

<span data-ttu-id="334ab-113">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="334ab-113">**REG\_DWORD**</span></span>

 

 



