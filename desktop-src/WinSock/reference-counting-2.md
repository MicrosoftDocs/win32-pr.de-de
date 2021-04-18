---
description: Ein Prozess ruft möglicherweise wspclosesocket für einen duplizierten Socket auf, und die Zuordnung des Deskriptors wird aufgehoben. Der zugrunde liegende Socket bleibt jedoch geöffnet, bis wspclosesocket für den letzten verbleibenden Deskriptor aufgerufen wird.
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: Verweis Zählung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72d9ef7b3e5e31cc7941d30c47f107fc068489ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354609"
---
# <a name="reference-counting"></a>Verweis Zählung

Ein Prozess ruft möglicherweise [**wspclosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) für einen duplizierten Socket auf, und die Zuordnung des Deskriptors wird aufgehoben. Der zugrunde liegende Socket bleibt jedoch geöffnet, bis **wspclosesocket** für den letzten verbleibenden Deskriptor aufgerufen wird.

 

 
