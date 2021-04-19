---
description: Die \_ forcecodepage-Tabelle ist eine spezielle Tabelle zum Ändern der Codepage eines Installationspakets. Sie können die Codepage bestimmen oder festlegen, indem Sie eine Textarchiv Datei mit dem Namen \_ forcecodepage. IDT exportieren oder importieren.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132843fa092409b26811afd6a4c1f3e7cf0544f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367889"
---
# <a name="_forcecodepage"></a>\_Forcecodepage

Die \_ forcecodepage-Tabelle ist eine spezielle Tabelle zum Ändern der Codepage eines Installationspakets. Sie können die Codepage bestimmen oder festlegen, indem Sie eine [Textarchiv Datei](text-archive-files.md) mit dem Namen \_ forcecodepage. IDT exportieren oder importieren.

Das Format der \_ forcecodepage-Tabelle ist 2 leere Zeilen, gefolgt von einer dritten Zeile, die die numerische Codepage angibt. Beispielsweise würde eine \_ forcecodepage Table. IDT-Datei für eine japanische Datenbank wie folgt aussehen. Die numerische Codepage ist in diesem Fall 932.

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

Weitere Informationen zur Verwendung \_ von forcecodepage zum Anzeigen oder Festlegen der Codepage einer Datenbank finden Sie in den folgenden Themen.

-   [Code Page Behandlung (Windows Installer)](code-page-handling-windows-installer-.md)
-   [Festlegen der Codepage einer Installations Datenbank](determining-an-installation-database-s-code-page.md)
-   [Festlegen der Codepage einer Datenbank](setting-the-code-page-of-a-database.md)

Die \_ forcecodepage-Tabelle ist eine spezielle Pseudo Tabelle, die zum Ändern der Codepage eines Installationspakets verwendet wird. Durch die Verwendung der \_ forcecodepage-Tabelle wird die-Datenbank auf die Codepage festgelegt, ohne dass eine Validierung durchgeführt wird, um zu überprüfen, ob die aktuell in der Datenbank vorhandenen Daten in die neue Codepage übersetzt werden Es wird immer empfohlen, die Codepage einer Datenbank mit einer sprach neutralen Datenbank zu ändern.

 

 



