---
title: Empfangen von angefordertem Datenverkehr über Teredo
description: Teredo bietet eine globale Konnektivität mithilfe von IPv6-und NAT-Traversale-Funktionen.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5c7ffe7b84cfa325b3ecd8c0858ad96445e629
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729041"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a><span data-ttu-id="dbd50-103">Empfangen von angefordertem Datenverkehr über Teredo</span><span class="sxs-lookup"><span data-stu-id="dbd50-103">Receiving Unsolicited Traffic Over Teredo</span></span>

<span data-ttu-id="dbd50-104">[Teredo](about-teredo.md) bietet eine globale Konnektivität mithilfe von IPv6-und NAT-Traversale-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="dbd50-104">[Teredo](about-teredo.md) provides global connectivity using IPv6 and NAT traversal capabilities.</span></span> <span data-ttu-id="dbd50-105">Viele Anwendungen, einschließlich Peer-to-Peer, erfordern jedoch, dass Teredo nicht angeforderten Datenverkehr aus dem Internet empfängt.</span><span class="sxs-lookup"><span data-stu-id="dbd50-105">However, many applications, including peer-to-peer, will require Teredo to receive unsolicited traffic from the Internet.</span></span> <span data-ttu-id="dbd50-106">Eine Anwendung kann so programmiert werden, dass Sie Datenverkehr über eine einzelne IPv6-Schnittstelle oder alle IPv6-fähigen Schnittstellen empfängt.</span><span class="sxs-lookup"><span data-stu-id="dbd50-106">An application can be programmed to receive traffic over a single IPv6 interface or all IPv6-capable interfaces.</span></span> <span data-ttu-id="dbd50-107">Diese Dokumentation beschreibt die Anforderungen für Anwendungen, die die Teredo-Schnittstelle verwenden, um nicht angeforderten IPv6-Datenverkehr zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="dbd50-107">This documentation describes the requirements for applications that use the Teredo interface to receive unsolicited IPv6 traffic.</span></span>

<span data-ttu-id="dbd50-108">Eine Anwendung empfängt den nicht angeforderten Datenverkehr über die Teredo-Schnittstelle nur dann, wenn die Anwendung bei der [Windows-Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page)registriert ist.</span><span class="sxs-lookup"><span data-stu-id="dbd50-108">An application will receive unsolicited traffic over the Teredo interface only if the application is registered with [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page).</span></span> <span data-ttu-id="dbd50-109">Um nicht angeforderten Datenverkehr zu empfangen, muss Folgendes eintreten:</span><span class="sxs-lookup"><span data-stu-id="dbd50-109">In order to receive unsolicited traffic the following must occur:</span></span>

-   <span data-ttu-id="dbd50-110">Benutzer müssen angewiesen werden, mit der Microsoft Management Console (MMC) die Option "Edge-Traversal" für eine Anwendung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="dbd50-110">Users must be instructed to use of the Microsoft Management Console (MMC) to enable the "Edge Traversal" option for an application.</span></span> <span data-ttu-id="dbd50-111">Diese Option ist unter Windows-Firewall Snap-In--> <application name> -> Registerkarte "Erweitert" verfügbar. Die Option "Edge-Traversal" muss für jede Anwendung einzeln aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="dbd50-111">This option is available under Windows Firewall Snap-In --> <application name> --> "Advanced" tab. The "Edge Traversal" option must be enabled individually for each application.</span></span>

-   <span data-ttu-id="dbd50-112">Die Option "Edge-Traversal" wird von der Anwendung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="dbd50-112">The "Edge Traversal" option is enabled by the application.</span></span> <span data-ttu-id="dbd50-113">Anwendungen, die nicht angeforderten Datenverkehr empfangen können, um sich bei der Windows-Firewall für "Edge-Traversal" zu registrieren und nicht angeforderten Datenverkehr über die Teredo-Schnittstelle empfangen zu können</span><span class="sxs-lookup"><span data-stu-id="dbd50-113">It is possible for applications capable of receiving unsolicited traffic to register with Windows Firewall for "Edge Traversal" and receive unsolicited traffic over the Teredo interface.</span></span> <span data-ttu-id="dbd50-114">Zu diesem Zweck muss eine Anwendung die [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) -API mit der Option "Edge Traversal" (Edgeausnahme) auf Variant true aufzurufen \_ .</span><span class="sxs-lookup"><span data-stu-id="dbd50-114">To do this an application must call the [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) API with the "Edge Traversal" option set to VARIANT\_TRUE.</span></span> <span data-ttu-id="dbd50-115">Die Benutzer Zustimmung ist für diesen API-Rückruf erforderlich, bevor eine Anwendung auf den Datenverkehr lauschen darf.</span><span class="sxs-lookup"><span data-stu-id="dbd50-115">User consent is required for this API call before an application is permitted to listen for the traffic.</span></span>

-   <span data-ttu-id="dbd50-116">Die Anwendung legt die Winsock [IPv6 \_ - \_ schutzebenensocketoption](/windows/desktop/WinSock/ipv6-protection-level) auf eine **\_ \_ uneingeschränkte Schutz Ebene** über [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)fest.</span><span class="sxs-lookup"><span data-stu-id="dbd50-116">The application sets the Winsock [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) socket option to **PROTECTION\_LEVEL\_UNRESTRICTED** via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span> <span data-ttu-id="dbd50-117">Dadurch kann die Anwendung Edge-Traversal-Datenverkehr empfangen.</span><span class="sxs-lookup"><span data-stu-id="dbd50-117">This will allow the application to receive Edge Traversal traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbd50-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dbd50-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbd50-119">Empfangen von angeforderten Datenverkehr über Teredo</span><span class="sxs-lookup"><span data-stu-id="dbd50-119">Receiving Solicited Traffic Over Teredo</span></span>](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 