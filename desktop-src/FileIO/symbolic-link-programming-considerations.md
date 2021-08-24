---
description: Überlegungen zur Programmierung bei der Arbeit mit symbolischen Verknüpfungen.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Überlegungen zur Programmierung (lokale Dateisysteme)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a98c244dac3fb4a9f6b73d11067af64512e0cfd54e58078bd87a2582b0c2de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981880"
---
# <a name="programming-considerations-local-file-systems"></a>Überlegungen zur Programmierung (lokale Dateisysteme)

Beachten Sie beim Arbeiten mit symbolischen Verknüpfungen die folgenden Programmierüberlegungen:

-   Symbolische Verknüpfungen können auf ein nicht vorhandenes Ziel verweisen.
-   Beim Erstellen einer symbolischen Verknüpfung überprüft das Betriebssystem nicht, ob das Ziel vorhanden ist.
-   Wenn eine Anwendung versucht, ein nicht vorhandenes Ziel zu öffnen, wird **ERROR \_ FILE NOT \_ \_ FOUND** zurückgegeben.
-   Symbolische Verknüpfungen sind Wiederholungspunkte. Weitere Informationen finden Sie unter [Bestimmen, ob ein Verzeichnis ein eingebundener Ordner ist.](determining-whether-a-directory-is-a-volume-mount-point.md)
-   In einem bestimmten Pfad sind maximal 63 Wiederholungspunkte (und somit symbolische Verknüpfungen) zulässig.

    **Windows Server 2003 und Windows XP:** Für einen bestimmten Pfad gilt ein Grenzwert von 31 Wiederholungspunkten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>


</dt> <dt>

[Hard Links and Junctions](hard-links-and-junctions.md)
</dt> </dl>

 

 



