---
description: Zum Erstellen einer kompletten Liste der Volumes auf einem Computer oder zum Bearbeiten der einzelnen Volumes können Sie Volumes auflisten.
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: Auflisten von Volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353561"
---
# <a name="enumerating-volumes"></a>Auflisten von Volumes

Zum Erstellen einer kompletten Liste der Volumes auf einem Computer oder zum Bearbeiten der einzelnen Volumes können Sie Volumes auflisten. Innerhalb eines Volumes können Sie nach bereitgestellten [Ordnern](enumerating-volume-mount-points.md) oder anderen Objekten auf dem Volume suchen.

Mit drei Funktionen kann eine Anwendung Volumes auf einem Computer aufzählen:

-   [**Findfirstvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [**Findnextvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [**Findvolumeclose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

Diese drei Funktionen funktionieren ähnlich wie die Funktionen " [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)", " [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)" und " [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) ".

Beginnen Sie mit der Suche nach Volumes mit " [**findfirstvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)". Wenn die Suche erfolgreich ist, verarbeiten Sie die Ergebnisse gemäß dem Design Ihrer Anwendung. Verwenden Sie dann [**findnextvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) in einer Schleife, um jedes nachfolgende Volume zu suchen und zu verarbeiten. Wenn die Bereitstellung von Volumes erschöpft ist, schließen Sie die Suche mit [**findvolumeclose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).

Sie sollten keine Korrelation zwischen der Reihenfolge der Volumes, die von diesen Funktionen zurückgegeben werden, und der Reihenfolge der Volumes annehmen, die von anderen Funktionen oder Tools zurückgegeben werden. Nehmen Sie insbesondere keine Korrelation zwischen der volumereihenfolge und den Laufwerk Buchstaben, die vom BIOS (sofern vorhanden) oder dem Datenträger Administrator zugewiesen wurden.

Ein Beispiel für die Aufzählung der Volumes auf einem Computer finden Sie unter Beispiele für bereitgestellte [Ordner](volume-mount-point-examples.md) .

 

 



