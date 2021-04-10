---
description: Ein Anforderer sollte nur dann einen bestimmten Anbieter auswählen, wenn er einige Informationen zu den verfügbaren Anbietern enthält.
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: Auswählen von Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39435f8f34091ccef51a6cce85b2c596f0c687d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131256"
---
# <a name="selecting-providers"></a>Auswählen von Anbietern

Ein Anforderer sollte nur dann einen bestimmten Anbieter auswählen, wenn er einige Informationen zu den verfügbaren Anbietern enthält.

Da dies in der Regel nicht der Fall ist, wird empfohlen, dass eine Anforderer die GUID \_ null als Anbieter-ID für [**IVssBackupComponents:: addtosnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)bereitstellt, wodurch das System einen Anbieter nach folgendem Algorithmus auswählen kann:

1.  Wenn ein Hardware Anbieter verfügbar ist, der das angegebene Volume unterstützt, wird er ausgewählt.
2.  Wenn kein Hardware Anbieter verfügbar ist, wird ein beliebiger Softwareanbieter ausgewählt, der für das jeweilige Volume spezifisch ist.
3.  Wenn kein Hardware Anbieter und kein Softwareanbieter für die Volumes verfügbar ist, wird der Systemanbieter ausgewählt.

Allerdings kann ein Anforderer mithilfe von [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)Informationen zu verfügbaren Anbietern abrufen. Mit diesen Informationen und nur dann, wenn die Sicherungs Anwendung ein gutes Verständnis der verschiedenen Anbieter hat, kann ein Anforderer eine gültige Anbieter-ID für [**IVssBackupComponents:: addtosnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)angeben.

Beachten Sie, dass alle Volumes nicht denselben Anbieter aufweisen müssen.

 

 



