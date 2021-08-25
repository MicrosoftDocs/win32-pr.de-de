---
description: Mit zunehmender Anzahl von Zertifikaten, Zertifikatsperrlisten (Certificate Revocation Lists, CRLs) und Zertifikatvertrauenslisten (Certificate Trust List, CTLs) in der Sammlung eines Benutzers wird die Organisation dieser Zertifikate zu einem Problem.
ms.assetid: 13e7e077-e8be-4ba4-99e1-08421fd2452e
title: Sammlungsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d783aafe6d0ff22cd990195f6bce5ce433f2f01595bed2cf20c5c41ea3a24e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876914"
---
# <a name="collection-stores"></a>Sammlungsspeicher

Mit zunehmender Anzahl von [*Zertifikaten,*](../secgloss/c-gly.md)Zertifikatsperrlisten (Certificate [*Revocation Lists,*](../secgloss/c-gly.md) CRLs) und Zertifikatvertrauenslisten (Certificate [*Trust List,*](../secgloss/c-gly.md) CTLs) in der Sammlung eines Benutzers wird die Organisation dieser Zertifikate zu einem Problem. Eine mögliche Lösung besteht in der Erstellung separater Zertifikatspeicher, um verschiedene Arten von Zertifikaten zu behalten. Diese Lösung verursacht ein neues Problem, da eine Anwendung möglicherweise mehrere verschiedene Speicher durchsuchen muss, um ein bestimmtes Zertifikat zu finden. Dieses Problem wird durch die Verwendung logischer Speicher oder Sammlungsspeicher gelöst.

Ein [*logischer Speicher*](../secgloss/l-gly.md) und ein Sammlungszertifikatspeicher sind Gruppen physischer Speicher, die einer Anwendung als einzelner Speicher angezeigt werden. Alle Memberspeicher eines logischen Speichers oder Sammlungsspeichers können mit einem einzigen Funktionsaufruf von [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) oder [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)durchsucht oder aufzählt werden.

Die Verwendung von logischen Speichern oder Sammlungsspeichern bietet auch Flexibilität, die mit Papierdatensätzen schwierig zu erreichen ist. Ein Zertifikat in einem einzelnen physischen Speicher muss möglicherweise Mitglied mehrerer verschiedener logischer Gruppen sein. Daher kann ein einzelner physischer Speicher Mitglied von mehr als einem logischen Speicher oder Sammlungsspeicher sein, wie in der folgenden Abbildung dargestellt.

![Sammlungsspeicher](images/mancert.png)

In dieser Abbildung werden die folgenden grundlegenden logischen Zertifikatspeicherkonzepte dargestellt:

-   Ein Sammlungszertifikatspeicher verfügt über einen Zeiger auf den ersten Zeigerblock für diesen Sammlungsspeicher.
-   Jeder Zeigerblock eines Sammlungsspeichers verfügt über einen Zeiger auf einen gleichgeordneten Speicher und einen Zeiger auf den nächsten Zeigerblock der Auflistung.
-   Jeder gleichgeordnete Speicher in einer Sammlung ist ein einfacher physischer Zertifikatspeicher.
-   Ein einfacher Zertifikatspeicher kann ein gleichgeordneter Mitgliedsspeicher in vielen verschiedenen Sammlungsspeichern sein.
-   Einem Sammlungsspeicher hinzugefügte Zertifikate werden physisch einem der gleichgeordneten Speicher in der Sammlung hinzugefügt.
-   Auf Zertifikate in einem gleichgeordneten Speicher kann von jedem Sammlungsspeicher zugegriffen werden, in dem der gleichgeordnete Speicher Mitglied ist.

Sammlungsspeicher werden in einer Anwendung erstellt, indem ein Sammlungsspeicher mithilfe von [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) geöffnet und dann [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection) verwendet wird, um dem Sammlungsspeicher einen geöffneten gleichgeordneten Speicher hinzuzufügen. Ein gleichgeordneter Speicher kann durch Aufrufen von [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection)aus einem Sammlungsspeicher gelöscht werden.

 

 
