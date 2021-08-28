---
description: Ein Prozess kann WSPCloseSocket für einen duplizierten Socket aufrufen, und die Zuordnung des Deskriptors wird freigegeben. Der zugrunde liegende Socket bleibt jedoch geöffnet, bis WSPCloseSocket für den letzten verbleibenden Deskriptor aufgerufen wird.
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: Verweiszählung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8cd281363636cc2022725b4921d3b2d2b300e7262173e157a2be1610f6af0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996660"
---
# <a name="reference-counting"></a>Verweiszählung

Ein Prozess kann [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) für einen duplizierten Socket aufrufen, und die Zuordnung des Deskriptors wird freigegeben. Der zugrunde liegende Socket bleibt jedoch geöffnet, bis **WSPCloseSocket** für den letzten verbleibenden Deskriptor aufgerufen wird.

 

 
