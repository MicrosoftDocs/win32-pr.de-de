---
description: Dieses Dokument enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit der Windows-Abbild Beschaffung (WIA).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Sicherheitsüberlegungen: Windows-Abbild Beschaffung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ab080582492a0c03eab7879624bfb49a370e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372831"
---
# <a name="security-considerations-windows-image-acquisition"></a><span data-ttu-id="5bfd2-103">Sicherheitsüberlegungen: Windows-Abbild Beschaffung</span><span class="sxs-lookup"><span data-stu-id="5bfd2-103">Security Considerations: Windows Image Acquisition</span></span>

<span data-ttu-id="5bfd2-104">Dieses Dokument enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit der Windows-Abbild Beschaffung (WIA).</span><span class="sxs-lookup"><span data-stu-id="5bfd2-104">This document provides information about security considerations related to Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="5bfd2-105">Dieses Dokument enthält nicht alles, was Sie über Sicherheitsprobleme wissen müssen, sondern als Ausgangspunkt und Verweis für diesen Technologiebereich.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-105">This document doesn't provide all you need to know about security issues - instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="5bfd2-106">Verwenden von Anführungszeichen um Pfadnamen</span><span class="sxs-lookup"><span data-stu-id="5bfd2-106">Use quotation marks around path names</span></span>](#use-quotation-marks-around-path-names)
-   [<span data-ttu-id="5bfd2-107">Platzieren registrierter Anwendungen an sicheren Orten</span><span class="sxs-lookup"><span data-stu-id="5bfd2-107">Place registered applications in secure locations</span></span>](#place-registered-applications-in-secure-locations)
-   [<span data-ttu-id="5bfd2-108">Verwenden Sie keine zugrunde liegenden Verzeichnisse oder Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-108">Do not use underlying directories or registry keys</span></span>](#do-not-use-underlying-directories-or-registry-keys)
-   [<span data-ttu-id="5bfd2-109">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5bfd2-109">Related Topics</span></span>](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a><span data-ttu-id="5bfd2-110">Verwenden von Anführungszeichen um Pfadnamen</span><span class="sxs-lookup"><span data-stu-id="5bfd2-110">Use quotation marks around path names</span></span>

<span data-ttu-id="5bfd2-111">Wenn Sie [**iwiadevmgr:: registereventcallbackprogram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) zum Registrieren einer Anwendung für den Empfang von Geräte Ereignissen verwenden, stellen Sie sicher, dass Sie den Pfad und den Dateinamen der Anwendung in Anführungszeichen einschließen.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-111">When using [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) to register an application to receive device events, be sure to surround the path and filename of the application with quotation marks.</span></span> <span data-ttu-id="5bfd2-112">Dadurch wird vermieden, dass der Pfad falsch interpretiert und eine nicht autorisierte Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-112">This avoids the possibility that the path is misinterpreted and an unauthorized application is run.</span></span>

## <a name="place-registered-applications-in-secure-locations"></a><span data-ttu-id="5bfd2-113">Platzieren registrierter Anwendungen an sicheren Orten</span><span class="sxs-lookup"><span data-stu-id="5bfd2-113">Place registered applications in secure locations</span></span>

<span data-ttu-id="5bfd2-114">Wenn eine Anwendung für den Empfang eines Geräte Ereignisses registriert ist, kann diese Anwendung von jedem Benutzer ausgeführt werden, der Zugriff auf das Gerät hat.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-114">When an application is registered to receive a device event, that application can be run by any user that has access to that device.</span></span> <span data-ttu-id="5bfd2-115">Wenn eine Anwendung z. b. für ein Scan Ereignis registriert ist, wird die Anwendung durch Drücken der Schaltfläche "überprüfen" auf einem Scanner ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-115">For example, if an application is registered for a scan event, pressing the "scan" button on a scanner will cause that application to run.</span></span> <span data-ttu-id="5bfd2-116">Wenn die Anwendung mit einer höheren Berechtigung als der Benutzer ausgeführt wird, verursacht dies ein potenzielles Sicherheitsproblem.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-116">If the application runs with a higher privilege than the user has, this causes a potential security issue.</span></span>

## <a name="do-not-use-underlying-directories-or-registry-keys"></a><span data-ttu-id="5bfd2-117">Verwenden Sie keine zugrunde liegenden Verzeichnisse oder Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-117">Do not use underlying directories or registry keys</span></span>

<span data-ttu-id="5bfd2-118">WIA verwendet intern mehrere Verzeichnisse und Registrierungsschlüssel zum Speichern von Daten oder Informationen.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-118">WIA uses several directories and registry keys internally to store data or information.</span></span> <span data-ttu-id="5bfd2-119">Greifen Sie nicht direkt auf diese Verzeichnisse oder Registrierungsschlüssel zu.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-119">Do not access these directories or registry keys directly.</span></span> <span data-ttu-id="5bfd2-120">Verwenden Sie stattdessen die verfügbar gemachten Schnittstellen Methoden, um Verzeichnisse für abgerufene Bilder anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5bfd2-120">Instead, use the exposed interface methods to specify directories for acquired images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5bfd2-121">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="5bfd2-121">Related Topics</span></span>

-   [<span data-ttu-id="5bfd2-122">Microsoft Security</span><span class="sxs-lookup"><span data-stu-id="5bfd2-122">Microsoft Security</span></span>](https://www.microsoft.com/security/)
-   [<span data-ttu-id="5bfd2-123">MSDN-Bibliotheks Sicherheit (Startseite)</span><span class="sxs-lookup"><span data-stu-id="5bfd2-123">MSDN Library Security Home Page</span></span>](https://msdn.microsoft.com/security/default.aspx)
-   [<span data-ttu-id="5bfd2-124">Gewusst-wie-Ressourcen für die Sicherheit</span><span class="sxs-lookup"><span data-stu-id="5bfd2-124">Security How-to Resources</span></span>](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [<span data-ttu-id="5bfd2-125">TechNet-Sicherheitsressourcen</span><span class="sxs-lookup"><span data-stu-id="5bfd2-125">TechNet Security Resources</span></span>](https://technet.microsoft.com/security/default.aspx)
-   <span data-ttu-id="5bfd2-126">[Sicherheitsüberlegungen für Windows XP Embedded-Entwickler](/previous-versions/ms838345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="5bfd2-126">[Security Considerations for Windows XP Embedded Developers](/previous-versions/ms838345(v=msdn.10))</span></span>
-   [<span data-ttu-id="5bfd2-127">Bewährte Sicherheitsmethoden</span><span class="sxs-lookup"><span data-stu-id="5bfd2-127">Security Best Practices</span></span>](../secbp/best-practices-for-the-security-apis.md)

 

 
