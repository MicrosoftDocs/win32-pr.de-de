---
description: Erben von manuellen Transaktionen
ms.assetid: 3616275c-1e2d-4f9d-8adf-11ac9be132f1
title: Erben von manuellen Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a802bb392223742e0116d34a81a25fe9be54f220
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340110"
---
# <a name="inheriting-manual-transactions"></a>Erben von manuellen Transaktionen

Wenn ein Objekt mit einer BYOT-Transaktion im Kontext ein zweites Objekt erstellt, kann das Downstream-Objekt die BYOT-Transaktion erben (sofern diese zum Erben von Transaktionen konfiguriert ist). Das erste mit dem BYOT-Gateway erstellte Objekt muss für "anfordern" oder "Support"-Transaktionen konfiguriert werden. Nachfolgende Objekte in der Aktivität können basierend auf den Anwendungsanforderungen konfiguriert werden.

Für automatische Transaktionen versucht die com+-Laufzeit nicht, einen Commit für die Transaktion auszuführen, bis das Stamm Objekt angibt, dass Sie bereit ist (durch Aufrufen von [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) vor der Rückgabe von einem Aufruf). Benutzer sollten sich bewusst sein, dass ein Commit für eine BYOT-Transaktion vorzeitig ausgeführt werden kann (da die Arbeit von untergeordneten Objekten noch nicht abgeschlossen wurde), da der Stamm nicht in der com+-Laufzeitumgebung ausgeführt wird und die Commit-Semantik nicht an die Lebensdauer des Objekts gebunden ist. Im Allgemeinen sollte der Benutzer darauf achten, dass die Synchronisierungs Grenze der Transaktion nicht verletzt wird.

Andernfalls wird die com+-Commit-Semantik angewendet. Com+ versucht nicht, einen Commit für eine Transaktion durchführen, während ein Objekt innerhalb einer Synchronisierungs Grenze aufgerufen wird. Außerdem können-Objekte ihre Konsistenz mithilfe von [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)angeben. Wenn versucht wird, einen Commit für eine Transaktion durchzusetzen, die die Arbeit eines Objekts mit dem Namen **DisableCommit** einschließt, wird die Transaktion abgebrochen.

 

 



