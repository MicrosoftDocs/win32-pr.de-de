---
title: Löschen einer Anwendungsverzeichnis Partition
description: Eine Anwendungsverzeichnis Partition wird gelöscht, indem das CrossRef-Objekt gelöscht wird, das die Anwendungsverzeichnis Partition darstellt.
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- Löschen einer Anwendungsverzeichnis-Partitions Anzeige
- Anwendungsverzeichnis Partitionen AD, löschen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd52ef99323ee7463a4733210314e02d911f0d66
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724576"
---
# <a name="deleting-an-application-directory-partition"></a>Löschen einer Anwendungsverzeichnis Partition

Eine Anwendungsverzeichnis Partition wird gelöscht, indem das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt gelöscht wird, das die Anwendungsverzeichnis Partition darstellt. Wenn das Löschen des **CrossRef** -Objekts auf einen Domänen Controller repliziert wird, der über ein Replikat der Anwendungsverzeichnis Partition verfügt, löscht die KCC das lokale Replikat der Anwendungsverzeichnis Partition. Dies bewirkt schließlich, dass alle Replikate der Anwendungsverzeichnis Partition gelöscht werden.

Wenn das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt gelöscht wird, löscht der Active Directory Server das [**domainDns**](/windows/desktop/ADSchema/c-domaindns) -Objekt, das beim Erstellen der Anwendungsverzeichnis Partition erstellt wurde, und löscht alle Objekte in der Anwendungsverzeichnis Partition. Keines der Objekte in der Anwendungsverzeichnis Partition wird gelöscht, wenn Sie gelöscht wurden.

Wenn eine Anwendungsverzeichnis Partition gelöscht wird, ist es sehr schwierig, Sie wiederherzustellen. Zum Wiederherstellen einer Anwendungsverzeichnis Partition ist es erforderlich, eine Sicherung mit einem Replikat der Anwendungsverzeichnis Partition wiederherzustellen, das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt zu suchen, das die Anwendungsverzeichnis Partition darstellt, und das **CrossRef** -Objekt autoritativ wiederherzustellen.

**Führen Sie die folgenden Schritte aus, um eine Anwendungsverzeichnis Partition und deren Replikate zu löschen.**

1.  Durchsuchen Sie den Container Partitionen nach einem [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt, das einen [**NCName**](/windows/desktop/ADSchema/a-ncname) -Attribut Wert aufweist, der gleich dem Distinguished Name der Anwendungsverzeichnis Partition ist.
2.  Löschen Sie das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt.

Weitere Informationen finden Sie unter [Beispiel Code zum Löschen einer Anwendungsverzeichnis Partition](example-code-for-deleting-an-application-directory-partition.md).

 

 