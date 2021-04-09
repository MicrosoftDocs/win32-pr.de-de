---
title: Remotedesktopprotokoll Anbieter Schnittstellen
description: Schnittstellen, die von der Remotedesktopprotokoll Anbieter-API unterstützt werden.
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85494e26c391095fbf97e8e408ee6b6181756c03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947304"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a><span data-ttu-id="bdae8-103">Remotedesktopprotokoll Anbieter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="bdae8-103">Remote Desktop Protocol Provider Interfaces</span></span>

<span data-ttu-id="bdae8-104">Die folgenden Schnittstellen werden von der Remotedesktopprotokoll Anbieter-API unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bdae8-104">The following interfaces are supported by the Remote Desktop Protocol Provider API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bdae8-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="bdae8-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="bdae8-106">**Iwrdsprodecolconnection**</span><span class="sxs-lookup"><span data-stu-id="bdae8-106">**IWRdsProtocolConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

<span data-ttu-id="bdae8-107">Macht Methoden verfügbar, die vom Remotedesktopdienste-Dienst aufgerufen werden, um eine Client Verbindung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="bdae8-107">Exposes methods called by the Remote Desktop Services service to configure a client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="bdae8-108">**Iwrdsproprocolconnectioncallback**</span><span class="sxs-lookup"><span data-stu-id="bdae8-108">**IWRdsProtocolConnectionCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

<span data-ttu-id="bdae8-109">Macht Methoden verfügbar, die Informationen über den Status einer Client Verbindung bereitstellen und Aktionen für den Client ausführen.</span><span class="sxs-lookup"><span data-stu-id="bdae8-109">Exposes methods that provide information about the status of a client connection and that perform actions for the client.</span></span> <span data-ttu-id="bdae8-110">Diese Schnittstelle wird vom Remotedesktopdienste-Dienst implementiert und durch das-Protokoll aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bdae8-110">This interface is implemented by the Remote Desktop Services service and called by the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="bdae8-111">**Iwrdspro| collicenseconnetction**</span><span class="sxs-lookup"><span data-stu-id="bdae8-111">**IWRdsProtocolLicenseConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

<span data-ttu-id="bdae8-112">Macht Methoden verfügbar, die vom Remotedesktopdienste-Dienst verwendet werden, um während einer Verbindungs Sequenz den Lizenzierungs Hand Shake auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bdae8-112">Exposes methods used by the Remote Desktop Services service to perform the licensing handshake during a connection sequence.</span></span>

</dd> <dt>

[<span data-ttu-id="bdae8-113">**Iwrdsprotekollistener**</span><span class="sxs-lookup"><span data-stu-id="bdae8-113">**IWRdsProtocolListener**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

<span data-ttu-id="bdae8-114">Macht Methoden verfügbar, die anfordern, dass das Protokoll auf Client Verbindungsanforderungen lauscht und die Überwachung beendet.</span><span class="sxs-lookup"><span data-stu-id="bdae8-114">Exposes methods that request that the protocol start and stop listening for client connection requests.</span></span>

</dd> <dt>

[<span data-ttu-id="bdae8-115">**Iwrdspro| collistenercallback**</span><span class="sxs-lookup"><span data-stu-id="bdae8-115">**IWRdsProtocolListenerCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

<span data-ttu-id="bdae8-116">Macht Methoden verfügbar, die den Remotedesktopdienste Dienst Benachrichtigen, dass ein Client eine Verbindung hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="bdae8-116">Exposes methods that notify the Remote Desktop Services service that a client has connected.</span></span>

</dd> <dt>

[<span data-ttu-id="bdae8-117">**Iwrdsproweredirector**</span><span class="sxs-lookup"><span data-stu-id="bdae8-117">**IWRdsProtocolLogonErrorRedirector**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

<span data-ttu-id="bdae8-118">Macht Methoden verfügbar, die vom Remotedesktopdienste Dienst aufgerufen werden, um den Anmeldestatus zu aktualisieren und zu bestimmen, wie Anmelde Fehlermeldungen umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="bdae8-118">Exposes methods called by the Remote Desktop Services service to update logon status and determine how to direct logon error messages.</span></span>

</dd> <dt>

[<span data-ttu-id="bdae8-119">**Iwrdsproum colmanager**</span><span class="sxs-lookup"><span data-stu-id="bdae8-119">**IWRdsProtocolManager**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

<span data-ttu-id="bdae8-120">Macht Methoden verfügbar, die der Remotedesktopdienste-Dienst für die Kommunikation mit dem Protokoll Anbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="bdae8-120">Exposes methods that the Remote Desktop Services service uses to communicate with the protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="bdae8-121">**Iwrdsprodecolsettings**</span><span class="sxs-lookup"><span data-stu-id="bdae8-121">**IWRdsProtocolSettings**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

<span data-ttu-id="bdae8-122">Macht Methoden zum Abrufen und Hinzufügen von Richtlinien bezogenen Einstellungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bdae8-122">Exposes methods for retrieving and adding policy-related settings.</span></span>

</dd> <dt>

[<span data-ttu-id="bdae8-123">**Iwrdsprotrocolshadowcallback**</span><span class="sxs-lookup"><span data-stu-id="bdae8-123">**IWRdsProtocolShadowCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

<span data-ttu-id="bdae8-124">Macht Methoden verfügbar, die vom Protokoll aufgerufen werden, um den Remotedesktopdienste Dienst zu benachrichtigen, dass die Zielseite eines Schattens gestartet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdae8-124">Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow.</span></span>

</dd> <dt>

[<span data-ttu-id="bdae8-125">**Iwrdsprodecolshadowconnection**</span><span class="sxs-lookup"><span data-stu-id="bdae8-125">**IWRdsProtocolShadowConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

<span data-ttu-id="bdae8-126">Macht Methoden verfügbar, die den Protokoll Anbieter über den Status des Sitzungs shadoings benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="bdae8-126">Exposes methods that notify the protocol provider about the status of session shadowing.</span></span>

</dd> <dt>

[<span data-ttu-id="bdae8-127">**Iwrdsremotefxgraphicsconnection**</span><span class="sxs-lookup"><span data-stu-id="bdae8-127">**IWRdsRemoteFXGraphicsConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

<span data-ttu-id="bdae8-128">Macht Methoden verfügbar, die sich auf die Bearbeitung und das Verständnis von Grafiken in der Client Verbindung beziehen.</span><span class="sxs-lookup"><span data-stu-id="bdae8-128">Exposes methods relating to the manipulation and understanding of graphics on the client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="bdae8-129">Veraltete Desktop Protokoll-Anbieter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="bdae8-129">Deprecated Desktop Protocol Provider Interfaces</span></span>](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

<span data-ttu-id="bdae8-130">Die folgenden Schnittstellen sind veraltet und sollten nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdae8-130">The following interfaces have been deprecated and should no longer be used.</span></span> <span data-ttu-id="bdae8-131">Verwenden Sie für neue Projekte stattdessen die Schnittstellen der Schnittstellen für Remotedesktopprotokoll-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="bdae8-131">For new projects, use the Remote Desktop Protocol Provider Interfaces interfaces instead.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="bdae8-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bdae8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdae8-133">Remotedesktopprotokoll Anbieter Referenz</span><span class="sxs-lookup"><span data-stu-id="bdae8-133">Remote Desktop Protocol Provider Reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dt>

[<span data-ttu-id="bdae8-134">Remotedesktopprotokoll Anbieter Enumerationen</span><span class="sxs-lookup"><span data-stu-id="bdae8-134">Remote Desktop Protocol Provider Enumerations</span></span>](custom-remote-protocol-enumerations.md)
</dt> <dt>

[<span data-ttu-id="bdae8-135">Remotedesktopprotokoll Anbieter Strukturen</span><span class="sxs-lookup"><span data-stu-id="bdae8-135">Remote Desktop Protocol Provider Structures</span></span>](custom-remote-protocol-structures.md)
</dt> <dt>

[<span data-ttu-id="bdae8-136">Remotedesktopprotokoll Anbieter-Unions</span><span class="sxs-lookup"><span data-stu-id="bdae8-136">Remote Desktop Protocol Provider Unions</span></span>](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




