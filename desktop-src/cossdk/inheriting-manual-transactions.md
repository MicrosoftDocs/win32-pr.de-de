---
description: Erben manueller Transaktionen
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Erben manueller Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0042b7bb1e1545c44c44149c4605c9aabcbcc12fecebb974eb97f95da087b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896010"
---
# <a name="inheriting-manual-transactions"></a>Erben manueller Transaktionen

Wenn ein Objekt mit einer BYOT-Transaktion im Kontext ein zweites Objekt erstellt, kann das Downstreamobjekt die BYOT-Transaktion erben (sofern für das Erben von Transaktionen konfiguriert). Das erste Objekt, das mit dem BYOT-Gateway erstellt wurde, muss so konfiguriert werden, dass Transaktionen "erforderlich" oder "unterstützt" werden. Nachfolgende Objekte in der Aktivität können basierend auf den Anwendungsanforderungen konfiguriert werden.

Bei automatischen Transaktionen versucht die COM+-Runtime erst dann, einen Commit für die Transaktion durchzuführen, wenn das Stammobjekt angibt, dass sie bereit ist (durch Aufrufen von [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) vor der Rückgabe von einem Aufruf). Benutzer sollten beachten, dass eine BYOT-Transaktion einen vorzeitigen Commit ausführen könnte (da die Arbeit untergeordneter Objekte nicht abgeschlossen wurde), da der "Stamm" nicht unter der COM+-Laufzeitumgebung ausgeführt wird und die Commitsemantik nicht an die Lebensdauer des Objekts gebunden ist. Im Allgemeinen sollte der Benutzer darauf achten, die Synchronisierungsgrenze der Transaktion nicht zu verletzen.

Andernfalls wird die COM+-Commitsemantik angewendet. COM+ versucht nicht, einen Commit für eine Transaktion durchzuführen, während ein Objekt innerhalb einer Synchronisierungsgrenze aufruft. Darüber hinaus können Objekte ihre Konsistenz mit [**DisableCommit angeben.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) Wenn versucht wird, einen Commit für eine Transaktion zu unternehmen, die die Arbeit eines Objekts mit dem Namen **DisableCommit** enthält, wird die Transaktion abgebrochen.

 

 



