---
title: Kompatibilität von Windows 8.1 und Windows Server 2012 R2-Client und-Server
description: Kompatibilität von Windows 8.1 und Windows Server 2012 R2-Client und-Server
ms.assetid: 45C37E2D-3513-4708-A562-1426D2B832F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c46647dd9ad0f0baeae1ffb98905740a37f9530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515608"
---
# <a name="windows-81-and-windows-server-2012-r2-client-and-server-compatibility"></a><span data-ttu-id="f3b11-103">Kompatibilität von Windows 8.1 und Windows Server 2012 R2-Client und-Server</span><span class="sxs-lookup"><span data-stu-id="f3b11-103">Windows 8.1 and Windows Server 2012 R2 client and server compatibility</span></span>

<span data-ttu-id="f3b11-104">In diesem Abschnitt werden Änderungen im Betriebssystem beschrieben, auf die Sie besonders achten sollten, wenn Sie sich auf die potenziellen Auswirkungen auf vorhandene apps auswirken, und wie neue apps auf Clients, auf Servern oder auf Clients und Servern entworfen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="f3b11-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="f3b11-105">Im folgenden finden Sie eine Liste der Themen, die in diesem Abschnitt behandelt werden:</span><span class="sxs-lookup"><span data-stu-id="f3b11-105">Following is the list of topics covered in this section:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f3b11-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f3b11-106">In this section</span></span>



| <span data-ttu-id="f3b11-107">Thema</span><span class="sxs-lookup"><span data-stu-id="f3b11-107">Topic</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="f3b11-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3b11-108">Description</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="f3b11-109">Änderungen an der Betriebssystemversion in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f3b11-109">Operating system version changes in Windows 8.1</span></span>](operating-system-version-changes-in-windows-8-1.md)<br/>                                                                                                             |             |
| [<span data-ttu-id="f3b11-110">Bedarfs gesteuerte Installation von Windows-Komponenten</span><span class="sxs-lookup"><span data-stu-id="f3b11-110">Windows components installed on demand</span></span>](windows-components-installed-on-demand.md)<br/>                                                                                                                               |             |
| [<span data-ttu-id="f3b11-111">HTML-Schriftart-Fall Back-Verhalten</span><span class="sxs-lookup"><span data-stu-id="f3b11-111">HTML font fallback behavior</span></span>](html-font-fallback-behavior.md)<br/>                                                                                                                                                     |             |
| [<span data-ttu-id="f3b11-112">Windows 8.1 nur HTTPS-URIs und keine http-URIs zulässt.</span><span class="sxs-lookup"><span data-stu-id="f3b11-112">Windows 8.1 allows only https URIs, not http URIs</span></span>](windows-8-1-allows-only-https-uris--not-http-uris.md)<br/>                                                                                                         |             |
| [<span data-ttu-id="f3b11-113">Mouswheel-Eingabe für Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f3b11-113">Mousewheel input for Windows 8.1</span></span>](mousewheel-input-for-windows-8-1.md)<br/>                                                                                                                                           |             |
| [<span data-ttu-id="f3b11-114">Touchpad-Geräte mit Windows Precision</span><span class="sxs-lookup"><span data-stu-id="f3b11-114">Windows precision touchpad devices</span></span>](windows-precision-touchpad-devices.md)<br/>                                                                                                                                       |             |
| [<span data-ttu-id="f3b11-115">Hohe dpi-Informationen für Desktop-Apps in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f3b11-115">High DPI for desktop apps in Windows 8.1</span></span>](high-dpi-for-desktop-apps-in-windows-8-1.md)<br/>                                                                                                                           |             |
| [<span data-ttu-id="f3b11-116">Edge-Benutzeroberfläche wird in in-out-und Trägheit-Szenarios unterdrückt</span><span class="sxs-lookup"><span data-stu-id="f3b11-116">Edge UI is suppressed in  in-out-in  and  inertia  scenarios</span></span>](edge-ui-is-suppressed-in--in-out-in--and--inertia--scenarios.md)<br/>                                                                                   |             |
| [<span data-ttu-id="f3b11-117">Das Aufrufen von immsetconfiguration Manager Status () oder immgetanversionstatus () aus Windows Store-Apps wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f3b11-117">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>](calling-immsetconversionstatus---or-immgetconversionstatus---from-windows-store-apps-is-not-supported.md)<br/> |             |
| [<span data-ttu-id="f3b11-118">IME-modusmodell von pro Benutzer in Thread pro Thread geändert</span><span class="sxs-lookup"><span data-stu-id="f3b11-118">IME mode model changed from per-user to per-thread</span></span>](ime-mode-model-changed-from-per-user-to-per-thread.md)<br/>                                                                                                       |             |
| [<span data-ttu-id="f3b11-119">Eingabemethoden-Manager-APIs werden vom vereinfachten Chinesisch (IME) nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f3b11-119">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>](input-method-manager-apis-are-not-supported-by-simplified-chinese-ime.md)<br/>                                                                 |             |
| [<span data-ttu-id="f3b11-120">Einige ostasiatische IME-Software Eingabe Panels senden jetzt VKey.</span><span class="sxs-lookup"><span data-stu-id="f3b11-120">Some East Asian IME software input panels now send vKey</span></span>](some-east-asian-ime-software-input-panels-now-send-vkey.md)<br/>                                                                                             |             |



 

 

 





