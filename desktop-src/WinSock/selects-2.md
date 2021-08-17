---
description: In der ursprünglichen Socketschnittstelle von Berkeley Software Distribution (BSD) war die Select-Funktion die Standardfunktion (und nur) zum Abrufen von Netzwerkereignisanzeigen.
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: Wählt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c075d2b8b18de79c25852eb0949cc727a8f3474e39392cf6e0a50fc60390d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740922"
---
# <a name="selects"></a>Wählt

In der ursprünglichen Socketschnittstelle von Berkeley Software Distribution (BSD) war die [**Select-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-select) die Standardfunktion (und nur) zum Abrufen von Netzwerkereignisanzeigen. Für jeden Socket können Informationen zum Lese-, Schreib- oder Fehlerstatus abgelesen oder gewartet werden. Weitere Informationen finden Sie unter [**WSPSelect.**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) Beachten Sie, dass \_ FD-QOS für Netzwerkereignis bei diesem Ansatz nicht ermittelt werden kann.

 

 
