---
title: Schreiben von Daten mithilfe eines DVC-Kanals
description: Das Schreiben von Kanaldaten mithilfe eines dynamischen virtuellen Kanals (DVC) ist sowohl für den Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server als auch für den Client symmetrisch.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd6f26e926958ceba5418a72849b75a66b11d2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338198"
---
# <a name="writing-data-by-using-a-dvc-channel"></a>Schreiben von Daten mithilfe eines DVC-Kanals

Das Schreiben von Kanaldaten mithilfe eines dynamischen virtuellen Kanals (DVC) ist sowohl für den Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server als auch für den Client symmetrisch. Das Schreiben von Kanaldaten wird von der [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) -Methode der [**iwzvirtualchannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) -Schnittstelle implementiert.

Die folgende Abbildung zeigt das Senden und empfangen des Datenpakets zwischen dem DVC-Client und-Server (DVC-Plug-in).

![Senden und Empfangen eines Datenpakets zwischen dem DVC-Client und-Server](images/writedvcchannel.png)

 

 




