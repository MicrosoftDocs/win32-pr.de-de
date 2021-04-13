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
# <a name="connection-sequence"></a>Verbindungs Sequenz

Die folgende Abbildung zeigt die Methodenaufrufe zwischen dem Remotedesktopdienste-Dienst und Ihrem Protokoll während der Client Verbindungs Sequenz. Die hier gezeigten Aktionen folgen der [Start Sequenz](start-sequence.md). Die Interaktion zwischen dem-Dienst und dem [**iwrdsprodecollicenseconnetction**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) -Objekt stellt den Lizenzierungs Hand Shake für den Client dar.

![Client Verbindungs Sequenz](images/protocol-connectionsequence.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Methoden aufrufssequenz](method-call-sequence.md)
</dt> <dt>

[Sequenz neu verbinden](reconnect-sequence.md)
</dt> <dt>

[Start Sequenz](start-sequence.md)
</dt> </dl>

 

 




