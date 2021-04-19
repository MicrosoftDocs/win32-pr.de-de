---
description: Ab Windows 8 ist die AppInit- \_ DLLs-Infrastruktur deaktiviert, wenn der sichere Start aktiviert ist.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: AppInit-DLLs und sicherer Start
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2915dda53959f2a403a62112385fe80e735cbfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359515"
---
# <a name="appinit-dlls-and-secure-boot"></a><span data-ttu-id="0a2fa-103">AppInit-DLLs und sicherer Start</span><span class="sxs-lookup"><span data-stu-id="0a2fa-103">AppInit DLLs and Secure Boot</span></span>

<span data-ttu-id="0a2fa-104">Ab Windows 8 ist die AppInit- \_ DLLs-Infrastruktur deaktiviert, wenn der sichere Start aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-104">Starting in Windows 8, the AppInit\_DLLs infrastructure is disabled when secure boot is enabled.</span></span>

## <a name="about-appinit_dlls"></a><span data-ttu-id="0a2fa-105">Informationen zu AppInit- \_ DLLs</span><span class="sxs-lookup"><span data-stu-id="0a2fa-105">About AppInit\_DLLs</span></span>

<span data-ttu-id="0a2fa-106">Die AppInit- \_ DLLs-Infrastruktur bietet eine einfache Möglichkeit, um System-APIs zu verbinden, indem Sie zulässt, dass benutzerdefinierte DLLs in den Adressraum der einzelnen interaktiven Anwendungen geladen werden.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-106">The AppInit\_DLLs infrastructure provides an easy way to hook system APIs by allowing custom DLLs to be loaded into the address space of every interactive application.</span></span> <span data-ttu-id="0a2fa-107">Anwendungen und Schadsoftware verwenden beide AppInit-DLLs aus demselben Grund, d. h. mit Hook-APIs. Nachdem die benutzerdefinierte DLL geladen wurde, kann Sie eine bekannte System-API anschließen und alternative Funktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-107">Applications and malicious software both use AppInit DLLs for the same basic reason, which is to hook APIs; after the custom DLL is loaded, it can hook a well-known system API and implement alternate functionality.</span></span> <span data-ttu-id="0a2fa-108">Nur ein kleiner Satz moderner legitimer Anwendungen verwendet diesen Mechanismus zum Laden von DLLs, während ein großer Satz Schadsoftware diesen Mechanismus verwendet, um Systeme zu gefährden.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-108">Only a small set of modern legitimate applications use this mechanism to load DLLs, while a large set of malware use this mechanism to compromise systems.</span></span> <span data-ttu-id="0a2fa-109">Selbst legitime AppInit \_ -DLLs können versehentlich zu System Deadlocks und Leistungsproblemen führen, weshalb die Verwendung von AppInit- \_ DLLs nicht empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-109">Even legitimate AppInit\_DLLs can unintentionally cause system deadlocks and performance problems, therefore usage of AppInit\_DLLs is not recommended.</span></span>

## <a name="appinit_dlls-and-secure-boot"></a><span data-ttu-id="0a2fa-110">AppInit \_ -DLLs und sicherer Start</span><span class="sxs-lookup"><span data-stu-id="0a2fa-110">AppInit\_DLLs and secure boot</span></span>

<span data-ttu-id="0a2fa-111">Windows 8 hat UEFI und sicheren Start eingesetzt, um die allgemeine Systemintegrität zu verbessern und einen starken Schutz vor anspruchsvollen Bedrohungen zu bieten.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-111">Windows 8 adopted UEFI and secure boot to improve the overall system integrity and to provide strong protection against sophisticated threats.</span></span> <span data-ttu-id="0a2fa-112">Wenn der sichere Start aktiviert ist, wird der AppInit- \_ DLLs-Mechanismus als Teil eines nicht kompromittierten Ansatzes deaktiviert, um Kunden vor Schadsoftware und Bedrohungen zu schützen.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-112">When secure boot is enabled, the AppInit\_DLLs mechanism is disabled as part of a no-compromise approach to protect customers against malware and threats.</span></span>

<span data-ttu-id="0a2fa-113">Beachten Sie, dass der sichere Start ein UEFI-Protokoll und kein Windows 8-Feature ist.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-113">Please note that secure boot is a UEFI protocol and not a Windows 8 feature.</span></span> <span data-ttu-id="0a2fa-114">Weitere Informationen zu UEFI und der Secure Boot Protocol-Spezifikation finden Sie unter [https://www.uefi.org](https://www.uefi.org/) .</span><span class="sxs-lookup"><span data-stu-id="0a2fa-114">More info on UEFI and the secure boot protocol specification can be found at [https://www.uefi.org](https://www.uefi.org/).</span></span>

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a><span data-ttu-id="0a2fa-115">AppInit \_ -DLLs-Zertifizierungs Anforderung für Windows 8-Desktop-Apps</span><span class="sxs-lookup"><span data-stu-id="0a2fa-115">AppInit\_DLLs certification requirement for Windows 8 desktop apps</span></span>

<span data-ttu-id="0a2fa-116">Eine der Zertifizierungsanforderungen für Windows 8-Desktop-Apps besteht darin, dass die APP keine beliebigen DLLs laden darf, um Win32-API-Aufrufe mithilfe des AppInit- \_ DLLs-Mechanismus abzufangen.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-116">One of the certification requirements for Windows 8 desktop apps is that the app must not load arbitrary DLLs to intercept Win32 API calls using the AppInit\_DLLs mechanism.</span></span> <span data-ttu-id="0a2fa-117">Ausführlichere Informationen zu den Zertifizierungsanforderungen finden Sie im Abschnitt 1,1 der [Zertifizierungsanforderungen für Windows 8-Desktop-Apps](../win_cert/certification-requirements-for-windows-desktop-apps.md).</span><span class="sxs-lookup"><span data-stu-id="0a2fa-117">For more detailed information about the certification requirements, refer to section 1.1 of [Certification requirements for Windows 8 desktop apps](../win_cert/certification-requirements-for-windows-desktop-apps.md).</span></span>

## <a name="summary"></a><span data-ttu-id="0a2fa-118">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0a2fa-118">Summary</span></span>

-   <span data-ttu-id="0a2fa-119">Der AppInit \_ -DLLs-Mechanismus ist keine empfohlene Vorgehensweise für legitime Anwendungen, da dies zu System Deadlocks und Leistungsproblemen führen kann.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-119">The AppInit\_DLLs mechanism is not a recommended approach for legitimate applications because it can lead to system deadlocks and performance problems.</span></span>
-   <span data-ttu-id="0a2fa-120">Der AppInit- \_ DLLs-Mechanismus ist standardmäßig deaktiviert, wenn der sichere Start aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0a2fa-120">The AppInit\_DLLs mechanism is disabled by default when secure boot is enabled.</span></span>
-   <span data-ttu-id="0a2fa-121">Die Verwendung von AppInit- \_ DLLs in einer Windows 8-Desktop-App ist ein Zertifizierungs Fehler bei der Windows-Desktop-App</span><span class="sxs-lookup"><span data-stu-id="0a2fa-121">Using AppInit\_DLLs in a Windows 8 desktop app is a Windows desktop app certification failure.</span></span>

<span data-ttu-id="0a2fa-122">Im folgenden Whitepaper finden Sie Informationen zu AppInit \_ -DLLs unter Windows 7 und Windows Server 2008 R2: [AppInit-DLLs in Windows 7 und Windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0a2fa-122">See the following whitepaper for info about AppInit\_DLLs on Windows 7 and Windows Server 2008 R2: [AppInit DLLs in Windows 7 and Windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).</span></span>

 

 
