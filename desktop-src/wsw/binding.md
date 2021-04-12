---
title: Kanalbindung
description: Bindungen geben das Wire-Protokoll und das lokale Verhalten eines Kanals an.
ms.assetid: 82d465c5-b23d-4403-b360-8c710fbc6e1c
keywords:
- Binden von Webdiensten für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723a729b87dc26849dbd1f84038805c5e47a0ea4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310288"
---
# <a name="channel-binding"></a><span data-ttu-id="dc829-106">Kanalbindung</span><span class="sxs-lookup"><span data-stu-id="dc829-106">Channel Binding</span></span>

<span data-ttu-id="dc829-107">Bindungen geben das Wire-Protokoll und das lokale Verhalten eines Kanals an.</span><span class="sxs-lookup"><span data-stu-id="dc829-107">Bindings specify the wire protocol and local behavior for a channel.</span></span> <span data-ttu-id="dc829-108">Bindungen bestehen aus den folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="dc829-108">Bindings are made up of the following components:</span></span>

-   <span data-ttu-id="dc829-109">Eine [**WS \_ - \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), die das zu verwendende Übertragungsprotokoll identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dc829-109">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), which identifies the transfer protocol to use.</span></span>
-   <span data-ttu-id="dc829-110">Eine [**WS- \_ Sicherheits \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), die angibt, wie der Kanal gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc829-110">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), which specifies how to secure the channel.</span></span>
-   <span data-ttu-id="dc829-111">Eine Set [**WS \_ Channel- \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), die zusätzliche optionale Einstellungen angibt (siehe auch [**ID der WS- \_ \_ Channeleigenschaft \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).</span><span class="sxs-lookup"><span data-stu-id="dc829-111">A set [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, which specify additional optional settings (see also [**WS\_CHANNEL\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).</span></span>

 

 




