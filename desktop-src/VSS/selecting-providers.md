---
description: Eine Anfordernde sollte nur dann einen bestimmten Anbieter auswählen, wenn einige Informationen zu den verfügbaren Anbietern verfügbar sind.
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: Auswählen von Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2451f172a569a23ba4799c16f8598ade4e6fb011f051b7ba7d948c7a366f22e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124500"
---
# <a name="selecting-providers"></a>Auswählen von Anbietern

Eine Anfordernde sollte nur dann einen bestimmten Anbieter auswählen, wenn einige Informationen zu den verfügbaren Anbietern verfügbar sind.

Da dies in der Regel nicht der Fall ist, wird empfohlen, dass ein an anfordernder Benutzer GUID NULL als Anbieter-ID für \_ [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)angibt, wodurch das System einen Anbieter gemäß dem folgenden Algorithmus auswählen kann:

1.  Wenn ein Hardwareanbieter verfügbar ist, der das gegebene Volume unterstützt, wird es ausgewählt.
2.  Wenn kein Hardwareanbieter verfügbar ist, wird er ausgewählt, wenn ein für das bestimmte Volume spezifischer Softwareanbieter verfügbar ist.
3.  Wenn kein Hardwareanbieter und kein für die Volumes spezifischer Softwareanbieter verfügbar ist, wird der Systemanbieter ausgewählt.

Ein Anfrager kann jedoch Informationen zu verfügbaren Anbietern mithilfe von [**IVssBackupComponents::Query abrufen.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) Mit diesen Informationen und nur wenn die Sicherungsanwendung über gute Kenntnisse der verschiedenen Anbieter verfügt, kann ein An anfordernder Benutzer [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)eine gültige Anbieter-ID zur Verfügung stellen.

Beachten Sie, dass nicht alle Volumes über denselben Anbieter verfügen müssen.

 

 



