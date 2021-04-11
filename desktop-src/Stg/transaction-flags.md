---
title: Transaktionsflags
description: Ein-Objekt kann entweder im direkten oder im transaktiven Modus geöffnet werden.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581d21db07921fe6d635aac44ceed256fee4ad85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206928"
---
# <a name="transaction-flags"></a>Transaktionsflags

Ein-Objekt kann entweder im direkten oder im transaktiven Modus geöffnet werden. Wenn ein Objekt im direkten Modus geöffnet wird, werden die Änderungen sofort und dauerhaft vorgenommen. Wenn ein Objekt im transaktiven Modus geöffnet wird, werden die Änderungen gepuffert, sodass Sie nach Abschluss der Bearbeitung explizit committet oder wieder hergestellt werden können. Geänderte Änderungen werden im-Objekt gespeichert, während wiederhergestellte Änderungen verworfen werden. Der direkte Modus ist der Standard Zugriffsmodus.

Der transaktive Modus ist auf einem übergeordneten Speicher Objekt nicht erforderlich, um ihn für ein untergeordnetes Element zu verwenden. Eine Transaktion für ein geschachteltes Element ist jedoch innerhalb der Transaktion für das übergeordnete Speicher Objekt geschachtelt. Daher kann für Änderungen, die an einem untergeordneten Objekt vorgenommen werden, erst dann ein Commit ausgeführt werden, wenn für das übergeordnete Objekt ein Commit ausgeführt wurde und für beide ein Commit ausgeführt wird, bis das Stamm Speicher Objekt (das übergeordnete Element der obersten Ebene) tatsächlich auf den Anders ausgedrückt: die Änderungen werden nach außen verschoben: innere Objekte veröffentlichen Änderungen an den Transaktionen ihrer unmittelbaren Container.

 

 




