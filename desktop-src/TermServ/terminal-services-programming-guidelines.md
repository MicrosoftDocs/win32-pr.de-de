---
title: Programmier Richtlinien für Remotedesktopdienste
description: Themen, in denen Richtlinien zum Entwickeln von Anwendungen in einer Remotedesktopdienste Umgebung bereitgestellt werden.
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste, Programmier Richtlinien
- Programmier Richtlinien Remotedesktopdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e767740a2f279c90ce4f0eb37c49919749465ad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339495"
---
# <a name="remote-desktop-services-programming-guidelines"></a><span data-ttu-id="10067-105">Programmier Richtlinien für Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="10067-105">Remote Desktop Services programming guidelines</span></span>

<span data-ttu-id="10067-106">Die meisten vorhandenen Windows-basierten 32-Bit-oder 64-Bit-Anwendungen werden "unverändert" in einer Remotedesktopdienste-Umgebung (ehemals "Terminal Services" genannt) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="10067-106">Most existing 32-bit or 64-bit Windows-based applications run "as is" in a Remote Desktop Services (formerly known as Terminal Services) environment.</span></span> <span data-ttu-id="10067-107">Einige Anwendungen funktionieren jedoch ordnungsgemäß und funktionieren gut in einer Remotedesktopdienste Umgebung, andere hingegen nicht.</span><span class="sxs-lookup"><span data-stu-id="10067-107">However, some applications function correctly and perform well in a Remote Desktop Services environment, while others do not.</span></span> <span data-ttu-id="10067-108">Die folgenden Themen bieten Richtlinien für die Entwicklung von Anwendungen in einer Remotedesktopdienste Umgebung.</span><span class="sxs-lookup"><span data-stu-id="10067-108">The following topics provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="10067-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="10067-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="10067-110">Richtlinien für mehrere Benutzer</span><span class="sxs-lookup"><span data-stu-id="10067-110">Multiple-user guidelines</span></span>](multiple-user-guidelines.md)
</dt> <dd>

<span data-ttu-id="10067-111">Richtlinien für die Entwicklung von Anwendungen für mehrere Benutzer in einer Remotedesktopdienste Umgebung.</span><span class="sxs-lookup"><span data-stu-id="10067-111">Guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="10067-112">Leistungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="10067-112">Performance guidelines</span></span>](performance-guidelines.md)
</dt> <dd>

<span data-ttu-id="10067-113">Richtlinien für die Entwicklung von Anwendungen, die in einer Remotedesktopdienste Umgebung eine gute Leistung erbringen.</span><span class="sxs-lookup"><span data-stu-id="10067-113">Guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="10067-114">Allgemeine Programmier Richtlinien</span><span class="sxs-lookup"><span data-stu-id="10067-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="10067-115">Richtlinien für die Entwicklung von Anwendungen in einer Remotedesktopdienste Umgebung.</span><span class="sxs-lookup"><span data-stu-id="10067-115">Guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> </dl>

<span data-ttu-id="10067-116">Viele dieser Richtlinien sind gute Programmierverfahren, die Anwendungen profitieren, die in jeder Windows-Umgebung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="10067-116">Many of these guidelines are good programming practices that will benefit applications running in any Windows environment.</span></span> <span data-ttu-id="10067-117">Einige empfohlene Optimierungen, wie z. b. das Einschränken von grafischen Effekten, sind jedoch Optimierungen, die Sie nur dann wünschen, wenn Ihre Anwendung unter Remotedesktopdienste ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10067-117">However, some recommended optimizations, such as limiting graphic effects, are optimizations that you would want only when your application is running under Remote Desktop Services.</span></span> <span data-ttu-id="10067-118">Ein Codebeispiel, in dem gezeigt wird, wie eine Remotedesktopdienste Umgebung erkannt wird, finden Sie unter [erkennen der Remotedesktopdienste Umgebung](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="10067-118">For a code example that shows how to detect a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="10067-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="10067-119">Related topics</span></span>

<dl> <span data-ttu-id="10067-120"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="10067-120"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="10067-121">Terminal Dienste sind jetzt Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="10067-121">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="10067-122">Format der administrativen Vorlagen Datei</span><span class="sxs-lookup"><span data-stu-id="10067-122">Administrative Template File Format</span></span>](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[<span data-ttu-id="10067-123">Sicherheit und Zugriffsrechte für den Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="10067-123">Registry Key Security and Access Rights</span></span>](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[<span data-ttu-id="10067-124">Registrierungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="10067-124">Registry Hives</span></span>](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[<span data-ttu-id="10067-125">Sicherheitsbeschreibungen</span><span class="sxs-lookup"><span data-stu-id="10067-125">Security Descriptors</span></span>](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[<span data-ttu-id="10067-126">Standard Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="10067-126">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="10067-127">Access Control Modell</span><span class="sxs-lookup"><span data-stu-id="10067-127">Access Control Model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 