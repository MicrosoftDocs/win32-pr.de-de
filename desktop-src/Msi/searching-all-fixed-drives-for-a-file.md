---
description: Während einer Windows Installer Installation kann das Installationsprogramm alle Festplattenlaufwerke nach einer Datei durchsuchen.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Suchen aller Festplattenlaufwerke nach einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b79c7f2999d4ee7937790dc68470210f1d4b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350291"
---
# <a name="searching-all-fixed-drives-for-a-file"></a>Suchen aller Festplattenlaufwerke nach einer Datei

**So durchsuchen Sie alle Festplattenlaufwerke nach einer Datei**

1.  Geben Sie die Datei Signatur und den Namen in der [Signatur Tabelle](signature-table.md)ein. Die verbleibenden Felder in diesem Datensatz können NULL sein, um nach einer beliebigen Version von MyApp.exe zu suchen.

    [Signatur Tabelle](signature-table.md) (partiell)

    

    | Signatur          | Dateiname            |
    |--------------------|----------------------|
    | Appfile<br/> | MyApp.exe<br/> |

    

     

2.  Geben Sie die Eigenschaft ein, die vom Installationsprogramm festgelegt werden soll, wenn MyApp.exe installiert ist.

    [AppSearch-Tabelle](appsearch-table.md)

    

    | Eigenschaft         | Signatur          |
    |------------------|--------------------|
    | MyApp<br/> | Appfile<br/> |

    

     

3.  Verwenden Sie die [drlocator-Tabelle](drlocator-table.md). Lassen Sie die Felder für übergeordnetes und Pfad leer, um alle Festplattenlaufwerke des Benutzer Systems zu durchsuchen. Geben Sie in der Spalte Tiefe die Anzahl der zu durchsuchenden Unterverzeichnis Ebenen an. Wenn Sie z. b. Tiefe auf 0 festlegen, wird c: \\MyApp.exe erkannt, aber die Datei wird nicht mit einer Tiefe von 2 erkannt, z. b.: c: \\ Program Files \\ myApps \\MyApp.exe.

    [Drlocator-Tabelle](drlocator-table.md)

    

    | Signatur          | Parent | Pfad | Tiefe        |
    |--------------------|--------|------|--------------|
    | Appfile<br/> |        |      | 3<br/> |

    

     

4.  Fügen Sie die Aktion AppSearch in die Aktions Sequenz ein. Wenn MyApp.exe installiert ist, legt das Installationsprogramm die Eigenschaft "MyApp" auf den Speicherort der Datei fest. Wenn die Datei installiert ist, wertet MyApp den Wert true in einem bedingten Ausdruck aus.

 

 




