---
title: Windows-Internet
description: Mit der Microsoft Windows Internet (WinInet) Application Programming Interface (API) können Anwendungen auf standardmäßige Internet Protokolle wie FTP und http zugreifen. Zur Erleichterung der Verwendung abstrahiert WinInet diese Protokolle in eine Oberfläche auf hoher Ebene.
ms.assetid: 9d1856ac-f281-4582-bb70-83a8ec674914
keywords:
- Windows Internet Wininet
- WinInet WinInet, Portal
- Windows Internet Wininet, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b5b76fefea900d3f187deb89929d3a09fe3c78
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473852"
---
# <a name="windows-internet"></a><span data-ttu-id="aef51-107">Windows-Internet</span><span class="sxs-lookup"><span data-stu-id="aef51-107">Windows Internet</span></span>

## <a name="purpose"></a><span data-ttu-id="aef51-108">Zweck</span><span class="sxs-lookup"><span data-stu-id="aef51-108">Purpose</span></span>

<span data-ttu-id="aef51-109">Mit der Microsoft Windows Internet (WinInet) Application Programming Interface (API) können Anwendungen auf standardmäßige Internet Protokolle wie FTP und http zugreifen.</span><span class="sxs-lookup"><span data-stu-id="aef51-109">The Microsoft Windows Internet (WinINet) application programming interface (API) enables applications to access standard Internet protocols, such as FTP and HTTP.</span></span> <span data-ttu-id="aef51-110">Zur Erleichterung der Verwendung abstrahiert WinInet diese Protokolle in eine Oberfläche auf hoher Ebene.</span><span class="sxs-lookup"><span data-stu-id="aef51-110">For ease of use, WinINet abstracts these protocols into a high-level interface.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="aef51-111">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="aef51-111">Where applicable</span></span>

<span data-ttu-id="aef51-112">WinInet unterstützt keine Server Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="aef51-112">WinINet does not support server implementations.</span></span> <span data-ttu-id="aef51-113">Außerdem sollte Sie nicht von einem Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aef51-113">In addition, it should not be used from a service.</span></span> <span data-ttu-id="aef51-114">Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="aef51-114">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="aef51-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="aef51-115">Developer audience</span></span>

<span data-ttu-id="aef51-116">WinInet ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="aef51-116">WinINet is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="aef51-117">Hierfür ist ein grundlegendes Verständnis der FTP-und HTTP-Protokolle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="aef51-117">It requires a basic understanding of the FTP and HTTP protocols.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="aef51-118">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="aef51-118">Run-time requirements</span></span>

<span data-ttu-id="aef51-119">Anwendungen, die die WinInet-API verwenden, benötigen Windows NT 4,0 oder höher oder Windows Me/98/95.</span><span class="sxs-lookup"><span data-stu-id="aef51-119">Applications that use the WinINet API require Windows NT 4.0 or later, or Windows Me/98/95.</span></span> <span data-ttu-id="aef51-120">Weitere Informationen dazu, welche Betriebssysteme oder Komponenten für die Verwendung eines bestimmten Programmier Elements erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="aef51-120">For more information about which operating systems or components are required to use a particular programming element, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aef51-121">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="aef51-121">In this section</span></span>



| <span data-ttu-id="aef51-122">Thema</span><span class="sxs-lookup"><span data-stu-id="aef51-122">Topic</span></span>                                                          | <span data-ttu-id="aef51-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aef51-123">Description</span></span>                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="aef51-124">Informationen zu Windows Internet</span><span class="sxs-lookup"><span data-stu-id="aef51-124">About Windows Internet</span></span>](about-wininet.md)<br/>         | <span data-ttu-id="aef51-125">Allgemeine Informationen zur Windows Internet-API.</span><span class="sxs-lookup"><span data-stu-id="aef51-125">General information about the Windows Internet API.</span></span><br/>   |
| [<span data-ttu-id="aef51-126">Verwenden von Windows Internet</span><span class="sxs-lookup"><span data-stu-id="aef51-126">Using Windows Internet</span></span>](using-wininet.md)<br/>         | <span data-ttu-id="aef51-127">Programmier Handbuch für die Windows Internet-API.</span><span class="sxs-lookup"><span data-stu-id="aef51-127">Programming guide for the Windows Internet API.</span></span><br/>       |
| [<span data-ttu-id="aef51-128">Windows-Internet Referenz</span><span class="sxs-lookup"><span data-stu-id="aef51-128">Windows Internet Reference</span></span>](wininet-reference.md)<br/> | <span data-ttu-id="aef51-129">Referenz Dokumentation für die Windows Internet-API.</span><span class="sxs-lookup"><span data-stu-id="aef51-129">Reference documentation for the Windows Internet API.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="aef51-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aef51-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aef51-131">Microsoft Windows HTTP-Dienste (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="aef51-131">Microsoft Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

