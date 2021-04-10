---
description: Wenn der Wert dieser pro-Computer-System Richtlinie auf &\# 0034; 2&0034 festgelegt ist \# , wird das Installationsprogramm für alle Anwendungen immer deaktiviert. Wenn dieser Richtlinien Wert auf &\# 0034; 1&0034; festgelegt ist \# , ist das Installationsprogramm für nicht verwaltete Anwendungen deaktiviert, aber weiterhin für verwaltete Anwendungen aktiviert.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf8a784f5e8090bf6ba2007091c22cf4bc070c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042395"
---
# <a name="disablemsi"></a><span data-ttu-id="8320f-104">DisableMSI</span><span class="sxs-lookup"><span data-stu-id="8320f-104">DisableMSI</span></span>

<span data-ttu-id="8320f-105">Wenn der Wert dieser pro-Computer- [System Richtlinie](system-policy.md) auf "2" festgelegt ist, wird das Installationsprogramm für alle Anwendungen immer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8320f-105">If the value of this per-machine [system policy](system-policy.md) is set to "2" the installer is always disabled for all applications.</span></span> <span data-ttu-id="8320f-106">Wenn dieser Richtlinien Wert auf "1" festgelegt ist, ist das Installationsprogramm für nicht verwaltete Anwendungen deaktiviert, aber weiterhin für verwaltete Anwendungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8320f-106">If this policy value is set to "1", the installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span>

<span data-ttu-id="8320f-107">In der folgenden Tabelle sind die möglichen Konfigurationen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8320f-107">The following table lists the possible configurations.</span></span>



| <span data-ttu-id="8320f-108">DisableMSI</span><span class="sxs-lookup"><span data-stu-id="8320f-108">DisableMSI</span></span> | <span data-ttu-id="8320f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8320f-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8320f-110">*Standard*</span><span class="sxs-lookup"><span data-stu-id="8320f-110">*Default*</span></span>  | <span data-ttu-id="8320f-111">Bei Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 und Windows Server 2008 R2 ist der Windows Installer für verwaltete Anwendungen aktiviert, wenn der Richtlinien Wert NULL, nicht vorhanden oder eine andere Zahl als 1 oder 2 ist.</span><span class="sxs-lookup"><span data-stu-id="8320f-111">On Windows Server 2003, Windows Server 2003 R2, Windows Server 2008, and Windows Server 2008 R2, if the policy value is Null, absent, or any number other than 1 or 2, the Windows Installer is enabled for managed applications.</span></span> <span data-ttu-id="8320f-112">Nicht verwaltete Anwendungs Installationen werden blockiert.</span><span class="sxs-lookup"><span data-stu-id="8320f-112">Unmanaged application installs are blocked.</span></span><br/> <span data-ttu-id="8320f-113">Unter Windows XP, Windows Vista und Windows 7 ist der Windows Installer für alle Anwendungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8320f-113">On Windows XP, Windows Vista, and Windows 7, the Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="8320f-114">Alle Installations Vorgänge sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="8320f-114">All install operations are allowed.</span></span><br/> |
| <span data-ttu-id="8320f-115">0</span><span class="sxs-lookup"><span data-stu-id="8320f-115">0</span></span>          | <span data-ttu-id="8320f-116">Windows Installer ist für alle Anwendungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8320f-116">Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="8320f-117">Alle Installations Vorgänge sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="8320f-117">All install operations are allowed.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8320f-118">1</span><span class="sxs-lookup"><span data-stu-id="8320f-118">1</span></span>          | <span data-ttu-id="8320f-119">Der Windows Installer ist für nicht verwaltete Anwendungen deaktiviert, aber weiterhin für verwaltete Anwendungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8320f-119">The Windows Installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span> <span data-ttu-id="8320f-120">Nicht erhöhte Installationen pro Benutzer werden blockiert.</span><span class="sxs-lookup"><span data-stu-id="8320f-120">Non-elevated per-user installations are blocked.</span></span> <span data-ttu-id="8320f-121">Pro Benutzer-und Computer spezifische Installationen sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="8320f-121">Per-user elevated and per-machine installs are allowed.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="8320f-122">2</span><span class="sxs-lookup"><span data-stu-id="8320f-122">2</span></span>          | <span data-ttu-id="8320f-123">Windows Installer ist für alle Anwendungen immer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8320f-123">Windows Installer is always disabled for all applications.</span></span> <span data-ttu-id="8320f-124">Es sind keine Installationen zulässig, einschließlich Reparaturen, Neuinstallationen oder Bedarfs gesteuerte Installationen.</span><span class="sxs-lookup"><span data-stu-id="8320f-124">No installs are allowed including repairs, reinstalls, or on-demand installations.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a><span data-ttu-id="8320f-125">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="8320f-125">Registry Key</span></span>

<span data-ttu-id="8320f-126">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="8320f-126">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="8320f-127">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8320f-127">Data Type</span></span>

<span data-ttu-id="8320f-128">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8320f-128">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="8320f-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8320f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8320f-130">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8320f-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




