---
title: Auffinden eines bestimmten Treibers
description: Auffinden eines bestimmten Treibers
ms.assetid: d48dc313-4606-4f70-b2fe-ed99160e53fc
keywords:
- Audiokomprimierungs-Manager (ACM), suchen nach Treibern
- ACM (Audiokomprimierungs-Manager), suchen nach Treibern
- ACM-Beispiele, Auffinden von Treibern
- Suchen nach Treibern
- acmdriverenum-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d8e8198fdf3bc742c2705e1a83b3ea8036c80f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856755"
---
# <a name="finding-a-specific-driver"></a>Auffinden eines bestimmten Treibers

Möglicherweise möchten Sie, dass Ihre Anwendung eine Nachricht direkt an einen bestimmten Treiber sendet oder bestimmte Treiber aus der Liste identifiziert. Beispielsweise möchten Sie, dass Ihre Anwendung die Treiber identifiziert, die Filter unterstützen, und dann jeden Treiber Abfragen, um zu bestimmen, welche Filter Tags er unterstützt. Sie können die [**acmdriverenum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) -Funktion verwenden, um ein Handle für die gewünschten Treiber oder Treiber zu erhalten. Dieses Handle kann dann verwendet werden, um mit diesem Treiber zu kommunizieren.

Beachten Sie, dass die [**acmdriveradd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) -Funktion ein Treiber handle zurückgibt, das für die Kommunikation mit dem Treiber verwendet werden kann, wenn eine Anwendung einen lokalen Treiber für die eigene Verwendung installiert. Es ist in diesem Fall nicht erforderlich, " **acmdriverenum** " zu verwenden.

 

 




