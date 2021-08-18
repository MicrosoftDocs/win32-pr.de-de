---
description: Während einer installation Windows Installer kann das Installationsprogramm alle Festplattenlaufwerke nach einer Datei durchsuchen.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Suchen aller Festplattenlaufwerke nach einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d460cd55fe54a98c6a02e23e49af9ea9838c7651262fa03f868bdb76acc2d506
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041250"
---
# <a name="searching-all-fixed-drives-for-a-file"></a>Suchen aller Festplattenlaufwerke nach einer Datei

**So durchsuchen Sie alle Festplattenlaufwerke nach einer Datei**

1.  Geben Sie die Dateisignatur und den Namen in die [Signaturtabelle ein.](signature-table.md) Die verbleibenden Felder in diesem Datensatz können NULL sein, um nach einer beliebigen Version der MyApp.exe.

    [Signaturtabelle](signature-table.md) (partiell)

    

    | Signatur          | Dateiname            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Geben Sie die Eigenschaft ein, die der Installer festlegen soll, MyApp.exe installiert ist.

    [AppSearch-Tabelle](appsearch-table.md)

    

    | Eigenschaft         | Signatur          |
    |------------------|--------------------|
    | Myapp<br/> | AppFile<br/> |

    

     

3.  Verwenden Sie die [DrLocator-Tabelle](drlocator-table.md). Lassen Sie die Felder Übergeordnetes Element und Pfad leer, um alle Festplattenlaufwerke des Benutzersystems zu durchsuchen. Geben Sie in der Spalte Tiefe die Anzahl der zu durchsuchenden Unterverzeichnisebenen an. Wenn Sie z. B. Depth auf 0 festlegen, wird c:MyApp.exe erkannt, die Datei jedoch nicht in einer Tiefe von 2, z. \\ B.: c: \\ Programme \\ MyApps \\MyApp.exe.

    [DrLocator-Tabelle](drlocator-table.md)

    

    | Signatur          | Parent | Pfad | Tiefe        |
    |--------------------|--------|------|--------------|
    | AppFile<br/> |        |      | 3<br/> |

    

     

4.  Schließen Sie die AppSearch-Aktion in die Aktionssequenz ein. Wenn MyApp.exe installiert ist, legt der Installer die Eigenschaft MYAPP auf den Speicherort der Datei fest. Wenn die Datei installiert ist, wird MYAPP in einem bedingten Ausdruck als True ausgewertet.

 

 




