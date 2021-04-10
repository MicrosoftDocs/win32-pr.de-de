---
description: Wenn die Anzahl der Zertifikate, Zertifikat Sperr Listen (CRLs) und Zertifikat Vertrauens Listen (CTLs) in der Sammlung eines Benutzers zunimmt, wird die Organisation dieser Zertifikate zu einem Problem.
ms.assetid: 13e7e077-e8be-4ba4-99e1-08421fd2452e
title: Sammlungs Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bfeb8ef071d7a5ccf6bc7ce43ba418117879536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867159"
---
# <a name="collection-stores"></a>Sammlungs Speicher

Wenn die Anzahl der [*Zertifikate*](../secgloss/c-gly.md), [*Zertifikat Sperr Listen*](../secgloss/c-gly.md) (CRLs) und [*Zertifikat Vertrauens Listen*](../secgloss/c-gly.md) (CTLs) in der Sammlung eines Benutzers zunimmt, wird die Organisation dieser Zertifikate zu einem Problem. Eine mögliche Lösung besteht darin, separate Zertifikat Speicher zu erstellen, um unterschiedliche Arten von Zertifikaten zu erhalten. Diese Lösung erstellt ein neues Problem, da eine Anwendung möglicherweise mehrere verschiedene Speicher durchsuchen muss, um ein bestimmtes Zertifikat zu finden. Das Problem wird durch die Verwendung logischer oder Sammlungs Speicher gelöst.

Ein [*Logischer Speicher*](../secgloss/l-gly.md) und ein Sammlungs Zertifikat Speicher sind Gruppen physischer Speicher, die einer Anwendung als einzelner Speicher angezeigt werden. Alle Element Speicher eines logischen Speichers oder eines Sammlungs Speichers können durchsucht oder mit einem einzelnen Funktions aufrufentweder von " [**certfindcertifitoreinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) " oder " [**certenumcertifitoresinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)" aufgezählt werden.

Die Verwendung logischer oder Sammlungs Speicher bietet auch eine größere Flexibilität bei Papier Datensätzen. Ein Zertifikat in einem einzelnen physischen Speicher muss möglicherweise Mitglied mehrerer logischer Gruppen sein. Daher kann ein einzelner physischer Speicher Mitglied von mehr als einem logischen oder Sammlungs Speicher sein, wie in der folgenden Abbildung dargestellt.

![Sammlungs Speicher](images/mancert.png)

Diese Abbildung zeigt die folgenden grundlegenden logischen Zertifikat Speicherkonzepte:

-   Ein Sammlungs Zertifikat Speicher weist einen Zeiger auf den ersten Zeiger Block für diesen Sammlungs Speicher auf.
-   Jeder Zeiger Block eines Sammlungs Speicher verfügt über einen Zeiger auf einen gleich geordneten Speicher und einen Zeiger auf den nächsten Zeiger Block der Auflistung.
-   Jeder gleich geordnete Speicher in einer Sammlung ist ein einfacher physischer Zertifikat Speicher.
-   Ein einfacher Zertifikat Speicher kann ein Mitglied eines gleich geordneten Speichers in vielen verschiedenen Sammlungs speichern sein.
-   Einem Sammlungs Speicher hinzugefügte Zertifikate werden physisch einem der gleich geordneten Speicher in der Auflistung hinzugefügt.
-   Auf Zertifikate in einem gleich geordneten Speicher kann von jedem Sammlungs Speicher zugegriffen werden, in dem der gleich geordnete Speicher ein Member ist.

Sammlungs Speicher werden in einer Anwendung erstellt, indem ein Sammlungs Speicher mithilfe von [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) geöffnet und dann mithilfe von [**certaddstoretocollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection) ein offener, gleich geordneter Speicher zum Sammlungs Speicher hinzugefügt wird. Ein gleich geordneter Speicher kann durch Aufrufen von [**certrerovestorefromcollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection)aus einem Sammlungs Speicher gelöscht werden.

 

 
