---
description: Zum Verwalten von Datensätzen können Sie mit Informationen arbeiten, die in Peer \_ Datensatzstrukturen gespeichert werden.
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Daten Satz Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c762689263e4a012bbdfad726b13e3ee8c79397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364066"
---
# <a name="record-management"></a>Daten Satz Verwaltung

Zum Verwalten von Datensätzen können Sie mit Informationen arbeiten, die in [**Peer \_ Daten Satz**](/windows/desktop/api/P2P/ns-p2p-peer_record) Strukturen gespeichert werden. Wenn Datensätze erstellt, aktualisiert oder gelöscht werden, werden die an einem Diagramm vorgenommenen Änderungen auf allen Knoten repliziert. In der folgenden Tabelle sind die Regeln zum Aktualisieren und automatischen Aktualisieren von Datensätzen aufgeführt.



| Verwaltungstask     | Regel                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktualisieren eines Datensatzes   | Behalten Sie die Ablaufzeit bei, oder erhöhen Sie Sie. Die Ablaufzeit kann nicht verringert werden.                                                                                                                      |
| Aktualisieren eines Datensatzes | Verwenden Sie zum automatischen Aktualisieren eines Datensatzes das Flag " [**\_ \_ \_ autoefresh" des Peer Datensatzes**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Verwenden Sie dieses Flag nur, wenn der Knoten, der einen Datensatz veröffentlicht, Online ist. Verwenden Sie andernfalls das Flag nicht. |



 

 

 



