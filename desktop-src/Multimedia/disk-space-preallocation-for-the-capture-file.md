---
title: Vorabzuordnung des Speicherplatzes für die Erfassungsdatei
description: Vorabzuordnung des Speicherplatzes für die Erfassungsdatei
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- WM_CAP_FILE_ALLOCATE-Nachricht
- capFileAlloc-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 687a14fa0f3a01a65ad2cb90062fcd4e237eb3e94ef99460d77883bd26df9213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678761"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a>Vorabzuordnung des Speicherplatzes für die Erfassungsdatei

Durch vorab zugewiesenen Speicherplatz für die Erfassungsdatei wird eine Datei mit einer angegebenen Größe auf dem Datenträger erstellt, bevor ein Erfassungsvorgang gestartet wird. Durch das Vorabbestellen einer Erfassungsdatei wird die Verarbeitung reduziert, die während der Erfassung erforderlich ist, und es werden weniger Frames gelöscht. Sie können eine Erfassungsdatei vorab zuordnen, indem Sie die [**WM \_ CAP FILE \_ \_ ALLOCATE-Nachricht**](wm-cap-file-allocate.md) (oder das [**Makro capFileAlloc)**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) verwenden.

In der Regel sollte Ihre Anwendung genügend Speicherplatz vorab zur Verfügung stellen, um die größte erwartete Erfassungsdatei zu enthalten. Durch das Vorabbelegung von Speicherplatz wird die Größe der erfassten Datei nicht beschränkt. Die Dateigröße wird automatisch vergrößert, wenn die erfassten Daten den zugeordneten Speicherplatz überschreiten. Nachfolgende Schreibvorgänge in die Erfassungsdatei wiederverwenden die Teile des Speicherplatzes, die der Datei zugeordnet sind, und bewahren die Größe und Fragmentierung der Datei auf.

Sie können die Erfassungsleistung auch verbessern, indem Sie die Erfassungsdatei defragmentieren. Verwenden Sie zum Defragmentieren der Datei ein Defragmentierungs-Hilfsprogramm, z. B. Datenträgerdefragmentierung. Wenn Sie eine defragmentierte Erfassungsdatei verwenden und später vergrößern, sollten Sie die vergrößerte Datei defragmentieren. Das Erweitern einer defragmentierten Erfassungsdatei kann den erweiterten Teil der Datei fragmentieren und die Leistung beim Erfassungsvorgang verringern.

Sie können auch die Leistung verbessern, indem Sie einen unkomprimierten Datenträger für die Videoaufnahme verwenden. Das Komprimieren von Daten während der Erfassung kann den Erfassungsdurchsatz auf dem Datenträger einschränken.

Eine Anwendung kann eine permanente Erfassungsdatei reservieren, um die Zeit zu vermeiden, die benötigt wird, um eine Datei bei jedem Start vorab zu defragmentieren und zu defragmentieren. Da eine Erfassungsdatei erheblichen Speicherplatz erfordern kann und durch vorab zugewiesene Erfassungsdatei alle Daten aus einer vorhandenen Erfassungsdatei entfernt werden, sollte eine Anwendung den Benutzer entscheiden lassen, ob die Datei dauerhaft oder temporär ist.

 

 




