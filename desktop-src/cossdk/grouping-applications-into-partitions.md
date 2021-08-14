---
description: Gruppieren von Anwendungen in Partitionen
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Gruppieren von Anwendungen in Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40491e95313544a32e23db78d8959736665db8c21782d3f1b30729e6eda6f1db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991100"
---
# <a name="grouping-applications-into-partitions"></a>Gruppieren von Anwendungen in Partitionen

Bei der Entscheidung, wie Anwendungen in Partitionen gruppiert werden sollen, müssen Administratoren bestimmte Regeln und Einschränkungen beachten, einschließlich der folgenden:

-   Eine Anwendung kann in einer oder mehreren Partitionen installiert werden.
-   In einer Anwendung kann nur eine Instanz einer bestimmten Komponente vorhanden sein.

## <a name="public-and-private-components"></a>Öffentliche und private Komponenten

Bei der Entscheidung, wie COM+-Anwendungen gruppiert werden sollen, gelten weitere Einschränkungen. Diese Einschränkungen gelten für öffentliche und private Komponenten innerhalb einer Anwendung. Anwendungskomponenten können im Allgemeinen entweder öffentlich oder privat sein. Beim Gruppieren von Anwendungen in Partitionen sollten Administratoren jedoch einige Einschränkungen in Bezug auf öffentliche und private Komponenten beachten. In der folgenden Tabelle sind diese Einschränkungen aufgeführt.



| Wenn eine Anwendung ist:              | Die Komponenten in einer Partition können dann folgende sein:                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Eine Serveranwendung<br/>    | Öffentlich und privat.<br/>                                                                                           |
| Eine Bibliotheksanwendung<br/>   | Nur öffentlich. Andernfalls könnte die Aufruferanwendung über die gleichen Komponenten verfügen, was zu Mehrdeutigkeit würde.<br/> |
| In der globalen Partition<br/> | Nur öffentlich. Dadurch wird Abwärtskompatibilität sichergestellt.<br/>                                                             |



 

## <a name="application-ids"></a>Anwendungs-IDs

Jede auf einem Computer installierte COM+-Anwendung verfügt über eine eindeutige Anwendungs-ID. Anwendungsnamen müssen jedoch nur innerhalb einer einzelnen Partition und nicht auf dem gesamten Computer eindeutig sein.

Die folgende Tabelle zeigt, was mit der Anwendungs-ID geschieht, wenn eine Anwendung in eine Partition importiert oder aus einer Partition exportiert wird.



| Wenn eine Anwendung ist:                                              | Dann die Anwendungs-ID:                    |
|--------------------------------------------------------------------|---------------------------------------------|
| In die globale Partition importiert<br/>                        | Bleibt unverändert<br/>                 |
| Importiert in eine andere Partition als die globale Partition<br/> | Wird geändert<br/>                       |
| Exportiert<br/>                                                | Ist in der exportierten Datei enthalten.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammeln von Partitionsmetriken](collecting-partition-metrics.md)
</dt> <dt>

[Konfigurieren des Partitionscaches](configuring-the-partition-cache.md)
</dt> <dt>

[Verwalten lokaler Partitionen](managing-local-partitions.md)
</dt> <dt>

[Verwalten von Partitionen in Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Festlegen von Administratorrechten für eine Partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




