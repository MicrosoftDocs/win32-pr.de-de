---
description: Zum Verwalten von Datensätzen können Sie mit Informationen arbeiten, die in PEER \_ RECORD-Strukturen gespeichert sind.
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Datensatzverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a747ae16e1773fe5944f2e9afdde8377d5e100a9a91316f70bcd1be8db6cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011518"
---
# <a name="record-management"></a>Datensatzverwaltung

Zum Verwalten von Datensätzen können Sie mit Informationen arbeiten, die in [**PEER \_ RECORD-Strukturen gespeichert**](/windows/desktop/api/P2P/ns-p2p-peer_record) sind. Wenn Datensätze erstellt, aktualisiert oder gelöscht werden, werden die an einem Graphen vorgenommenen Änderungen auf allen Knoten repliziert. In der folgenden Tabelle sind die Regeln zum Aktualisieren und automatischen Aktualisieren von Datensätzen aufgeführt.



| Verwaltungstask     | Regel                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktualisieren eines Datensatzes   | Behalten Sie die Ablaufzeit bei, oder erhöhen Sie sie. Sie können die Ablaufzeit nicht verringern.                                                                                                                      |
| Aktualisieren eines Datensatzes | Verwenden Sie das [**FLAG PEER RECORD FLAG \_ \_ \_ AUTOREFRESH,**](/windows/desktop/api/P2P/ns-p2p-peer_record) um einen Datensatz automatisch zu aktualisieren. Verwenden Sie dieses Flag nur, wenn der Knoten, der einen Datensatz veröffentlicht, online ist. Verwenden Sie andernfalls dieses Flag nicht. |



 

 

 



