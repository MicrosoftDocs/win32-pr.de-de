---
title: Verbindungs Sequenz
description: Eine Abbildung, in der die Methodenaufrufe zwischen dem Remotedesktopdienste-Dienst und Ihrem Protokoll während der Client Verbindungs Sequenz angezeigt werden.
ms.assetid: 60e56093-c457-43bc-b152-15c5acbfb016
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fe18d1a3b305a99fb0aaa35c51696f66de5c09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388656"
---
# <a name="connection-sequence"></a><span data-ttu-id="0f833-103">Verbindungs Sequenz</span><span class="sxs-lookup"><span data-stu-id="0f833-103">Connection Sequence</span></span>

<span data-ttu-id="0f833-104">Die folgende Abbildung zeigt die Methodenaufrufe zwischen dem Remotedesktopdienste-Dienst und Ihrem Protokoll während der Client Verbindungs Sequenz.</span><span class="sxs-lookup"><span data-stu-id="0f833-104">The following illustration shows the method calls made between the Remote Desktop Services service and your protocol during the client connection sequence.</span></span> <span data-ttu-id="0f833-105">Die hier gezeigten Aktionen folgen der [Start Sequenz](start-sequence.md).</span><span class="sxs-lookup"><span data-stu-id="0f833-105">The actions shown here follow the [Start Sequence](start-sequence.md).</span></span> <span data-ttu-id="0f833-106">Die Interaktion zwischen dem-Dienst und dem [**iwrdsprodecollicenseconnetction**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) -Objekt stellt den Lizenzierungs Hand Shake für den Client dar.</span><span class="sxs-lookup"><span data-stu-id="0f833-106">The interaction between the service and the [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) object represents the licensing handshake for the client.</span></span>

![Client Verbindungs Sequenz](images/protocol-connectionsequence.png)

## <a name="related-topics"></a><span data-ttu-id="0f833-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f833-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f833-109">Methoden aufrufssequenz</span><span class="sxs-lookup"><span data-stu-id="0f833-109">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="0f833-110">Sequenz neu verbinden</span><span class="sxs-lookup"><span data-stu-id="0f833-110">Reconnect Sequence</span></span>](reconnect-sequence.md)
</dt> <dt>

[<span data-ttu-id="0f833-111">Start Sequenz</span><span class="sxs-lookup"><span data-stu-id="0f833-111">Start Sequence</span></span>](start-sequence.md)
</dt> </dl>

 

 




