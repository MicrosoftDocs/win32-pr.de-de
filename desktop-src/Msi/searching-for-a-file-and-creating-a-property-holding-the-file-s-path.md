---
description: Während einer Windows Installer Installation kann das Installationsprogramm nach einer Datei suchen und eine Eigenschaft mit dem Pfad der Datei erstellen.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Suchen nach einer Datei und Erstellen einer Eigenschaft mit dem Pfad der Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed742ee874c2e4b76137e9f17e90fbf54e9729f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866064"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a>Suchen nach einer Datei und Erstellen einer Eigenschaft mit dem Pfad der Datei

**So suchen Sie nach einer Datei und erstellen eine Eigenschaft, die den Pfad der Datei enthält**

1.  Suchen Sie zuerst nach der Datei, indem Sie die Datei Signatur und den Namen in der [Signatur Tabelle](signature-table.md)auflisten.

    Die restlichen Felder dieses Datensatzes können leer gelassen werden, um eine Suche nach einer beliebigen Version von MyApp.exe anzugeben.

    [Signatur Tabelle](signature-table.md) (partiell)

    

    | Signatur          | Dateiname            |
    |--------------------|----------------------|
    | Appfile<br/> | MyApp.exe<br/> |

    

     

2.  Geben Sie als nächstes den Pfad der Datei an, nach der in der [drlocator-Tabelle](drlocator-table.md)gesucht wird.

    Da appfolder nicht in der [Signatur Tabelle](signature-table.md)aufgeführt ist, stellt das Installationsprogramm fest, dass appfolder ein Ordner und keine Datei ist.

    [Drlocator-Tabelle](drlocator-table.md)

    

    | Signatur            | Parent             | Pfad | Tiefe |
    |----------------------|--------------------|------|-------|
    | Appfile<br/>   |                    |      |       |
    | Appfolder<br/> | Appfile<br/> |      |       |

    

     

3.  Füllen Sie schließlich die [AppSearch-Tabelle](appsearch-table.md) auf, damit die [AppSearch-Aktion](appsearch-action.md) den Pfad von appfolder zurückgibt.

    Nachdem das Installationsprogramm die AppSearch-Aktion ausgeführt hat, ist der Wert von "MyFolder" der vollständige Pfad von "appfolder".

    [AppSearch-Tabelle](appsearch-table.md) (partiell)

    

    | Eigenschaft            | Signatur            |
    |---------------------|----------------------|
    | MYFOLDER<br/> | Appfolder<br/> |

    

     

 

 




