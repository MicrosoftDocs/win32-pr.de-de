---
description: Während einer installation Windows Installer kann das Installationsprogramm nach einer Datei suchen und eine Eigenschaft erstellen, die den Pfad der Datei enthält.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Suchen nach einer Datei und Erstellen einer Eigenschaft, die den Pfad der Datei enthält
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d1315616c6d2ea24052ddad85c005d53716f8b130f4aa2d23d69754c946416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041140"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a>Suchen nach einer Datei und Erstellen einer Eigenschaft, die den Pfad der Datei enthält

**So suchen Sie nach einer Datei und erstellen eine Eigenschaft, die den Pfad dieser Datei enthält**

1.  Suchen Sie zunächst nach der Datei, indem Sie die Dateisignatur und den Namen in der [Signaturtabelle auflisten.](signature-table.md)

    Die restlichen Felder dieses Datensatzes können leer gelassen werden, um eine Suche nach einer beliebigen Version von MyApp.exe.

    [Signaturtabelle](signature-table.md) (partiell)

    

    | Signatur          | Dateiname            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Geben Sie als Nächstes den Pfad der Datei an, nach der in der [DrLocator-Tabelle gesucht wird.](drlocator-table.md)

    Da AppFolder nicht in der Signaturtabelle [aufgeführt](signature-table.md)ist, bestimmt der Installer, dass AppFolder ein Ordner und keine Datei ist.

    [DrLocator-Tabelle](drlocator-table.md)

    

    | Signatur            | Parent             | Pfad | Tiefe |
    |----------------------|--------------------|------|-------|
    | AppFile<br/>   |                    |      |       |
    | AppFolder<br/> | AppFile<br/> |      |       |

    

     

3.  Füllen Sie abschließend die [AppSearch-Tabelle auf,](appsearch-table.md) damit die [AppSearch-Aktion](appsearch-action.md) den Pfad von AppFolder zurückgibt.

    Nachdem der Installer die AppSearch-Aktion ausgeführt hat, ist der Wert von MYFOLDER der vollständige Pfad von AppFolder.

    [AppSearch-Tabelle](appsearch-table.md) (partiell)

    

    | Eigenschaft            | Signatur            |
    |---------------------|----------------------|
    | Myfolder<br/> | AppFolder<br/> |

    

     

 

 




