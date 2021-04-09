---
description: Ein WMI-Hochleistungs Anbieter erhöht die Geschwindigkeit, mit der ein WMI-Client Informationen von einem WMI-Instanzanbieter abrufen kann.
ms.assetid: 767a16bb-44b6-4c56-b79b-23241fcc216e
ms.tgt_platform: multiple
title: Verbessern der Effizienz eines Instanzanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fecd0d8a20a3dcccd2878996823a7eb8a7ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866884"
---
# <a name="improving-the-efficiency-of-an-instance-provider"></a>Verbessern der Effizienz eines Instanzanbieters

Ein WMI-Hochleistungs Anbieter erhöht die Geschwindigkeit, mit der ein WMI-Client Informationen von einem WMI-Instanzanbieter abrufen kann. Die Haupt Änderung besteht darin, dass ein Hochleistungs Anbieter als Prozess interner Server sowohl für die Client Anwendung als auch für WMI ausgeführt wird. Wenn Sie den Anbieter innerhalb des Client Prozesses platzieren, können Sie die Interaktion zwischen den beiden beschleunigen.

Weitere Informationen zum Erstellen eines Hochleistungs Anbieters für den Instanzanbieter finden Sie unter Erstellen eines [Instanzanbieters in einen High-Performance-Anbieter](making-an-instance-provider-into-a-high-performance-provider.md).

 

 



