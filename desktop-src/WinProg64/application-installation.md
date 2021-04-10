---
title: Anwendungs Installation auf 64-Bit-Systemen
description: Der 64-Bit-Windows Installer kann auf 64-Bit-Windows-Anwendungen nahtlos auf 32-Bit-MSI-basierten Anwendungen installieren.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- Anwendungs Installation 64-Bit-Windows-Programmierung
- Installation 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101906"
---
# <a name="application-installation-on-64-bit-systems"></a><span data-ttu-id="ec9f3-105">Anwendungs Installation auf 64-Bit-Systemen</span><span class="sxs-lookup"><span data-stu-id="ec9f3-105">Application Installation on 64-bit Systems</span></span>

<span data-ttu-id="ec9f3-106">Der [64-Bit-Windows Installer](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) kann auf 64-Bit-Windows-Anwendungen nahtlos auf 32-Bit-MSI-basierten Anwendungen installieren.</span><span class="sxs-lookup"><span data-stu-id="ec9f3-106">The [64-bit Windows Installer](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span> <span data-ttu-id="ec9f3-107">Bei älteren Anwendungen, die einen 16-Bit-Stub zum Starten eines 32-Bit-Installations Moduls verwenden, erkennt das 64-Bit-Windows bestimmte Programme mit 16-Bit-Installer und ersetzt eine portierte 32-Bit-Version.</span><span class="sxs-lookup"><span data-stu-id="ec9f3-107">For older applications that use a 16-bit stub to launch a 32-bit installation engine, 64-bit Windows recognizes specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span>

<span data-ttu-id="ec9f3-108">16-Bit-DOS-, Windows-oder OS/2-Anwendungen verwenden häufig einen 16-Bit-Stub, um den Computertyp zu überprüfen, und starten dann eine 32-Bit-Installations-Engine, um die Installation tatsächlich auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ec9f3-108">16-bit DOS, Windows, or OS/2 applications often use a 16-bit stub to check the machine type, then launch a 32-bit installation engine to actually perform the installation.</span></span> <span data-ttu-id="ec9f3-109">Um die Installation von Anwendungen zu ermöglichen, die diese Technik verwenden, ersetzt 64-Bit-Windows 32-Bit-Versionen für die folgenden 16-Bit-Installer-Programme:</span><span class="sxs-lookup"><span data-stu-id="ec9f3-109">To enable installation of applications that use this technique, 64-bit Windows substitutes 32-bit versions for the following 16-bit installer programs:</span></span>

* <span data-ttu-id="ec9f3-110">Microsoft Setup für Windows 1,2</span><span class="sxs-lookup"><span data-stu-id="ec9f3-110">Microsoft Setup for Windows 1.2</span></span>  
* <span data-ttu-id="ec9f3-111">Microsoft Setup für Windows 2,6</span><span class="sxs-lookup"><span data-stu-id="ec9f3-111">Microsoft Setup for Windows 2.6</span></span>  
* <span data-ttu-id="ec9f3-112">Microsoft Setup für Windows 3,0</span><span class="sxs-lookup"><span data-stu-id="ec9f3-112">Microsoft Setup for Windows 3.0</span></span>  
* <span data-ttu-id="ec9f3-113">Microsoft Setup für Windows 3,01</span><span class="sxs-lookup"><span data-stu-id="ec9f3-113">Microsoft Setup for Windows 3.01</span></span>  
* <span data-ttu-id="ec9f3-114">InstallShield 5. x</span><span class="sxs-lookup"><span data-stu-id="ec9f3-114">InstallShield 5.x</span></span>  

<span data-ttu-id="ec9f3-115">Die Liste der Substitutionen wird in der Registrierung unter folgendem Schlüssel gespeichert: **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**.</span><span class="sxs-lookup"><span data-stu-id="ec9f3-115">The list of substitutions is stored in the registry under the following key: **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64**.</span></span>

> [!Note]  
> <span data-ttu-id="ec9f3-116">Dieser Mechanismus wird nur für die Kompatibilität mit 32-Bit-Anwendungen bereitgestellt, die die in diesem Thema aufgeführten 16-Bit-Microsoft Installer-Programme verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec9f3-116">This mechanism is provided only for compatibility with 32-bit applications that use the 16-bit Microsoft installer programs listed in this topic.</span></span> <span data-ttu-id="ec9f3-117">Das Hinzufügen von Installationsprogrammen von Drittanbietern wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec9f3-117">Addition of third-party installer programs is not supported.</span></span>

 

> [!Note]  
> <span data-ttu-id="ec9f3-118">Dieser Mechanismus ist nicht unter Windows 10 auf Arm enthalten.</span><span class="sxs-lookup"><span data-stu-id="ec9f3-118">This mechanism is not included on Windows 10 on ARM.</span></span>

 

 

 