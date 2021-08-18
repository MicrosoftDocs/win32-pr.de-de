---
title: Schreiben von Daten mithilfe eines DVC-Kanals
description: Das Schreiben von Kanaldaten mithilfe eines dynamischen virtuellen Kanals (DYNAMIC Virtual Channel, DVC) ist sowohl für den Remotedesktop-Sitzungshost server (RD-Sitzungshost) als auch für den Client symmetrisch.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e3f73b8e7a3d7db8ac109e84c9c638845af441b58568156782710fdac0968a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058243"
---
# <a name="writing-data-by-using-a-dvc-channel"></a>Schreiben von Daten mithilfe eines DVC-Kanals

Das Schreiben von Kanaldaten mithilfe eines dynamischen virtuellen Kanals (DYNAMIC Virtual Channel, DVC) ist sowohl für den Remotedesktop-Sitzungshost server (RD-Sitzungshost) als auch für den Client symmetrisch. Das Schreiben von Kanaldaten wird durch die [**Write-Methode**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) der [**IWTSVirtualChannel-Schnittstelle**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) implementiert.

Die folgende Abbildung zeigt das Senden und Empfangen des Datenpakets zwischen dem DVC-Client und dem Server (DVC-Plug-In).

![Senden und Empfangen eines Datenpakets zwischen dem DVC-Client und dem Server](images/writedvcchannel.png)

 

 




