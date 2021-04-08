---
title: Extensible Authentication-Protokoll Host
description: Erfahren Sie mehr über den EAP-Host (Extensible Authentication Protocol). Weitere Informationen finden Sie unter Lauf Zeitanforderungen und Anzeigen zusätzlicher verfügbarer Ressourcen.
ms.assetid: caaef367-2952-44fc-ac4c-f0db6387850e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f007435c43969ad0f195b0a6a1e697ab817d9c4
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104102594"
---
# <a name="extensible-authentication-protocol-host"></a><span data-ttu-id="6f360-104">Extensible Authentication-Protokoll Host</span><span class="sxs-lookup"><span data-stu-id="6f360-104">Extensible Authentication Protocol Host</span></span>

## <a name="purpose"></a><span data-ttu-id="6f360-105">Zweck</span><span class="sxs-lookup"><span data-stu-id="6f360-105">Purpose</span></span>


<span data-ttu-id="6f360-106">EAPHost ist eine Microsoft Windows-Netzwerkkomponente, die eine EAP-Infrastruktur (Extensible Authentication Protocol) für die Authentifizierung von "Supplicant"-Protokollimplementierungen wie [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) und [Point-to-Point](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP) bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6f360-106">EAPHost is a Microsoft Windows Networking component that provides an Extensible Authentication Protocol (EAP) infrastructure for the authentication of "supplicant" protocol implementations such as [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) and [Point-to-Point](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP).</span></span> <span data-ttu-id="6f360-107">Außerdem ermöglicht es die Authentifizierung mit "Authenticator"-Technologien wie Microsoft Network Policy Server (NPS).</span><span class="sxs-lookup"><span data-stu-id="6f360-107">It also allows for authentication with "authenticator" technologies such as the Microsoft network policy server (NPS).</span></span> <span data-ttu-id="6f360-108">Im Gegensatz zum vorherigen IAS-Server ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)) unterstützt NPS den [Netzwerk Zugriffsschutz (Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) , NAP).</span><span class="sxs-lookup"><span data-stu-id="6f360-108">Unlike the previous IAS Server ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS supports [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span></span>


<span data-ttu-id="6f360-109">Mithilfe der EAPHost-APIs können sich Anwendungen mithilfe des EAPHost-Diensts authentifizieren und eine Vorlage für die Entwicklung von Konformitäten Authentifizierungsmethoden für die Verwendung mit EAPHost bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6f360-109">The EAPHost APIs enable applications to authenticate using the EAPHost service, and provide a template for the development of conformant authentication methods for use with EAPHost.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6f360-110">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="6f360-110">Run-time requirements</span></span>

<span data-ttu-id="6f360-111">Die EAPHost-APIs werden nur in Windows Vista und höheren Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f360-111">The EAPHost APIs are supported only in Windows Vista and later operating systems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f360-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6f360-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f360-113">Informationen zu EAPHost</span><span class="sxs-lookup"><span data-stu-id="6f360-113">About EAPHost</span></span>](about-eap-host.md)
</dt> <dt>

[<span data-ttu-id="6f360-114">Verwenden von EAPHost</span><span class="sxs-lookup"><span data-stu-id="6f360-114">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="6f360-115">EAPHost-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="6f360-115">EAPHost API Reference</span></span>](eaphost-api-reference.md)
</dt> </dl>

 

 