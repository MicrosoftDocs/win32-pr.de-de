---
title: Vorab Zuordnung des Speicherplatzes für die Erfassungs Datei
description: Vorab Zuordnung des Speicherplatzes für die Erfassungs Datei
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- WM_CAP_FILE_ALLOCATE Meldung
- capfilezuweisung-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7442b08170fb6f018555c043c59d96860701ed4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309855"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a>Vorab Zuordnung des Speicherplatzes für die Erfassungs Datei

Durch die vorab Zuordnung von Speicherplatz für die Erfassungs Datei wird eine Datei mit einer angegebenen Größe auf dem Datenträger erstellt, bevor ein Aufzeichnungs Vorgang gestartet wird. Durch das vorab zuordnen einer Erfassungs Datei wird die während der Erfassung erforderliche Verarbeitung reduziert, und es werden weniger gelöschte Frames erzielt. Sie können eine Aufzeichnungsdatei vorab zuordnen, indem Sie [**die \_ \_ Datei \_**](wm-cap-file-allocate.md) Zuordnungs Nachricht der WM-Abdeckung (oder das [**capfilealloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) -Makro) verwenden.

In der Regel sollte Ihre Anwendung ausreichend Speicherplatz zuordnen, um die größte erwartete Erfassungs Datei zu enthalten. Durch die vorab Zuordnung von Speicherplatz wird die Größe der erfassten Datei nicht eingeschränkt. Die Dateigröße wird automatisch vergrößert, wenn die erfassten Daten den zugewiesenen Speicherplatz überschreiten. Bei nachfolgenden Schreibvorgängen in der Erfassungs Datei werden die für die Datei zugeordneten Teile des Speicherplatzes wieder verwendet, und die Größe und Fragmentierung der Datei werden beibehalten.

Sie können die Erfassungs Leistung auch verbessern, indem Sie die Erfassungs Datei defragmentieren. Verwenden Sie zum Defragmentieren der Datei ein Defragmentierungsdienstprogramm, z. b. Datenträger Defragmentierung. Wenn Sie eine defragmentierte Erfassungs Datei verwenden und Sie später vergrößern, sollten Sie die erweiterte Datei defragmentieren. Durch das Vergrößern einer defragmentierten Erfassungs Datei kann der erweiterte Teil der Datei fragmentiert und die Leistung beim Aufzeichnungs Vorgang reduziert werden.

Sie können die Leistung auch verbessern, indem Sie einen unkomprimierten Datenträger für die Video Erfassung verwenden. Durch das Komprimieren von Daten während der Erfassung kann der Aufzeichnungs Durchsatz auf den Datenträger beschränkt werden.

Eine Anwendung kann eine permanente Erfassungs Datei reservieren, um die erforderliche Zeit für das vorab zuordnen und Defragmentieren einer Datei zu vermeiden, wenn Sie gestartet wird. Da eine Aufzeichnungsdatei beträchtlichen Speicherplatz erfordern kann und die vorab Zuordnung einer Erfassungs Datei alle Daten aus einer vorhandenen Erfassungs Datei entfernt, sollte eine Anwendung den Benutzer entscheiden können, ob die Datei permanent oder temporär ist.

 

 




