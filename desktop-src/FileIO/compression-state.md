---
description: Jede Datei und jedes Verzeichnis auf einem Volume, das die Komprimierung für einzelne Dateien und Verzeichnisse unterstützt, hat einen Komprimierungs Status.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: Komprimierungs Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e182921a6c5e1b79c08fbafb6a8104c4bd8ca1cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216251"
---
# <a name="compression-state"></a>Komprimierungs Status

Jede Datei und jedes Verzeichnis auf einem Volume, das die Komprimierung für einzelne Dateien und Verzeichnisse unterstützt, hat einen *Komprimierungs Status*.

Während das Komprimierungs Attribut einer Datei oder eines Verzeichnisses lediglich angibt, ob die Datei oder das Verzeichnis komprimiert oder nicht komprimiert ist, wird im Komprimierungs Status auch das Format aller komprimierten Daten angegeben.

Verwenden Sie den Code für die [**FSCTL- \_ \_ Komprimierung**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) , um den Komprimierungs Status einer Datei oder eines Verzeichnisses zu ermitteln.

Der Komprimierungs Status wird als 16-Bit-Wert codiert. Der Komprimierungs Statuswert " \_ \_ None" gibt an, dass eine Datei nicht komprimiert ist. Der Standardwert für das Komprimierungs \_ Format \_ gibt an, dass eine Datei mit dem Standard Komprimierungs Format komprimiert wird. Jeder andere Wert gibt an, dass eine Datei komprimiert wird. dabei wird das vom Komprimierungs Zustandswert angegebene Komprimierungs Format verwendet.

Verwenden Sie den Code für die [**\_ \_ Komprimierung des FSCTL-Satzes**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) , um den Komprimierungs Status einer Datei oder eines Verzeichnisses festzulegen. Mit diesem Vorgang wird auch das Komprimierungs Attribut der Datei oder des Verzeichnisses festgelegt.

Wenn Sie den Komprimierungs Status einer Datei auf einen Wert ungleich 0 (null) festlegen, wird die Datei mit dem Komprimierungs Format komprimiert, das durch den Komprimierungs Zustandswert codiert ist Wenn Sie den Komprimierungs Status einer Datei auf NULL festlegen, wird die Datei von dekomprimiert. Dies sind synchrone Vorgänge. Wenn Sie den Komprimierungs Status festlegen, wird die Datei sofort komprimiert oder dekomprimiert.

Das Festlegen des Komprimierungs Zustands eines Verzeichnisses führt nicht zu einer sofortigen Komprimierung oder Komprimierung. Stattdessen wird beim Festlegen des Komprimierungs Zustands eines Verzeichnisses ein Standard Komprimierungs Status festgelegt, der allen neu erstellten Dateien und Unterverzeichnissen zugewiesen wird.

 

 
