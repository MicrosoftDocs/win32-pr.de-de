---
description: Die Funktionen certaddcertifierelinktostore, certaddcrllinktostore und certaddctllinktostore fügen Links zu vorhandenen Kontexten in Zertifikat Speicher hinzu, anstatt Kopien dieser Kontexte hinzuzufügen.
ms.assetid: 482fb11e-eb59-4de2-a2ad-c1960617e64b
title: Zertifikat Verknüpfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2954c52bcc7b2d98ab5ebb8d732abcbc8f0dea81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131445"
---
# <a name="certificate-links"></a>Zertifikat Verknüpfungen

Die Funktionen [**certaddcertifierelinktostore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), [**certaddcrllinktostore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)und [**certaddctllinktostore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) fügen Links zu vorhandenen Kontexten in [*Zertifikat Speicher*](../secgloss/c-gly.md) hinzu, anstatt Kopien dieser Kontexte hinzuzufügen. Durch das Hinzufügen von Links zu [*Speichern wird das*](../secgloss/c-gly.md)gleiche physische Zertifikat, die gleiche [*Zertifikat*](../secgloss/c-gly.md)Sperr Liste oder die gleiche [*CTL*](../secgloss/c-gly.md) über verschiedene Geschäfte verfügbar. Änderungen, die an den erweiterten Eigenschaften eines [*Kontexts*](../secgloss/c-gly.md) aus dem Speicher des ursprünglichen Kontexts oder aus einem Speicher, in dem ein Link zu diesem Kontext gespeichert ist, vorgenommen werden, sind im Speicher verfügbar, der den ursprünglichen Kontext und in allen anderen speichern mit Links zu diesem Kontext enthält.

Ein Beispiel für die Verwendung von [**certaddcertifikatelinktostore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)finden Sie unter [Beispiel C-Programm: Zertifikat Speichervorgänge](example-c-program-certificate-store-operations.md).

![Zertifikat Verknüpfungen](images/mancert1.png)

Angenommen, die Zertifikate A. 1, a. 2, a. 3 und a. 4 befinden sich ursprünglich in Store A, und die Zertifikate B. 1, b. 2, b. 3 und b. 4 befinden sich ursprünglich im Speicher b.

-   Das Diagramm zeigt einen Link, der in Store B zu Zertifikat a. 2 hinzugefügt wurde, und einen Link, der in Speicher a zu Zertifikat B hinzugefügt wurde. 2.
-   Das Original von Zertifikat a. 2 befindet sich immer noch im Speicher a. Das Original von B. 2 befindet sich noch im Speicher b.
-   Alle Änderungen, die an den erweiterten Eigenschaften von Zertifikat a. 2 oder Zertifikat b. 2 aus entweder Store a oder Store b vorgenommen werden, sind für beide Geschäfte verfügbar.
-   Wenn eine Kopie des Zertifikats a. 3 erstellt und im Speicher b gespeichert wurde, werden alle Änderungen an den erweiterten Eigenschaften des ursprünglichen a. 3-Zertifikats, die aus Speicher a erstellt wurden, in der neuen Kopie in Speicher b nicht angezeigt. Wenn an den erweiterten Eigenschaften der Kopie von Zertifikat A. 3 in Speicher B Änderungen vorgenommen wurden, wirken sich diese Änderungen nicht auf den Inhalt des ursprünglichen A. 3-Zertifikats aus und sind aus Speicher A nicht sichtbar.

 

 
