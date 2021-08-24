---
description: Jede Datei und jedes Verzeichnis auf einem Volume, das die Komprimierung für einzelne Dateien und Verzeichnisse unterstützt, weist einen Komprimierungsstatus auf.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: Komprimierungsstatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19abfe0deecb951c00dacb00c64dd8dcf7af56d37fe9112095cdce403619f843
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582420"
---
# <a name="compression-state"></a>Komprimierungsstatus

Jede Datei und jedes Verzeichnis auf einem Volume, das die Komprimierung für einzelne Dateien und Verzeichnisse unterstützt, weist den *Komprimierungsstatus* auf.

Während das Komprimierungsattribut einer Datei oder eines Verzeichnisses einfach angibt, ob die Datei oder das Verzeichnis komprimiert ist oder nicht, gibt der Komprimierungsstatus auch das Format aller komprimierten Daten an.

Verwenden Sie den [**FSCTL \_ GET \_ COMPRESSION-Steuerungscode,**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) um den Komprimierungsstatus einer Datei oder eines Verzeichnisses zu bestimmen.

Der Komprimierungszustand wird als 16-Bit-Wert codiert. Der Komprimierungszustandswert COMPRESSION \_ FORMAT \_ NONE gibt an, dass eine Datei nicht komprimiert ist. Der Wert COMPRESSION \_ FORMAT \_ DEFAULT gibt an, dass eine Datei mit dem Standardkomprimierungsformat komprimiert wird. Jeder andere Wert gibt an, dass eine Datei mit dem komprimierten Format komprimiert wird, das durch den Komprimierungszustandswert angegeben wird.

Verwenden Sie den [**FSCTL \_ SET COMPRESSION-Steuerungscode, \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) um den Komprimierungsstatus einer Datei oder eines Verzeichnisses festzulegen. Dieser Vorgang legt auch das Komprimierungsattribut der Datei oder des Verzeichnisses fest.

Durch Festlegen des Komprimierungsstatus einer Datei auf einen Wert ungleich 0 (null) wird die Datei mithilfe des Komprimierungsformats komprimiert, das durch den Komprimierungszustandswert codiert wird. Durch Festlegen des Komprimierungsstatus einer Datei auf 0 (null) wird die Datei dekomprimiert. Dies sind synchrone Vorgänge. Die Datei wird sofort komprimiert oder dekomprimiert, wenn Sie ihren Komprimierungsstatus festlegen.

Das Festlegen des Komprimierungszustands eines Verzeichnisses führt nicht zu einer sofortigen Komprimierung oder Dekomprimierung. Stattdessen legt das Festlegen des Komprimierungszustands eines Verzeichnisses einen Standardkomprimierungszustand fest, der allen neu erstellten Dateien und Unterverzeichnissen gewährt wird.

 

 
