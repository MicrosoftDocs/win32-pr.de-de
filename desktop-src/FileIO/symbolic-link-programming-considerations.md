---
description: Programmier Überlegungen für die Arbeit mit symbolischen Verknüpfungen.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Überlegungen zur Programmierung (lokale Dateisysteme)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5d63c231c88da95efc0e5078506bf9fc0d6d9a
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "106370351"
---
# <a name="programming-considerations-local-file-systems"></a>Überlegungen zur Programmierung (lokale Dateisysteme)

Beachten Sie beim Arbeiten mit symbolischen Verknüpfungen die folgenden Programmier Überlegungen:

-   Symbolische Verknüpfungen können auf ein nicht vorhandenes Ziel verweisen.
-   Beim Erstellen eines symbolischen Links überprüft das Betriebssystem nicht, ob das Ziel vorhanden ist.
-   Wenn eine Anwendung versucht, ein nicht vorhandenes Ziel zu öffnen, wird die **Fehler \_ Datei \_ nicht \_ gefunden** .
-   Symbolische Verknüpfungen sind Analyse Punkte. Weitere Informationen finden Sie unter [bestimmen, ob ein Verzeichnis ein](determining-whether-a-directory-is-a-volume-mount-point.md)bereitgestellter Ordner ist.
-   Es sind maximal 63 Analyse Punkte (und daher symbolische Verknüpfungen) in einem bestimmten Pfad zulässig.

    **Windows Server 2003 und Windows XP:** Es gibt ein Limit von 31 Analyse Punkten für einen beliebigen Pfad.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>


</dt> <dt>

[Feste Links und Verbindungen](hard-links-and-junctions.md)
</dt> </dl>

 

 



