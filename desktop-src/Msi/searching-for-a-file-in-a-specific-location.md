---
description: Während einer Windows Installer Installation kann das Installationsprogramm nach einer Datei an einem bestimmten Speicherort im System des Benutzers suchen.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Suchen nach einer Datei an einem bestimmten Speicherort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ad4e456d331119b698d8e6e696e86b953006eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529498"
---
# <a name="searching-for-a-file-in-a-specific-location"></a>Suchen nach einer Datei an einem bestimmten Speicherort

**So suchen Sie nach einer Datei an einem bestimmten Speicherort auf einem Benutzersystem**

1.  Listen Sie die Datei Signatur und den Namen in der [Signatur Tabelle](signature-table.md)auf. Die verbleibenden Felder in diesem Datensatz können NULL sein, um nach einer beliebigen Version von MyApp.exe zu suchen.

    [Signatur Tabelle](signature-table.md)

    

    | Signatur          | Dateiname            |
    |--------------------|----------------------|
    | Appfile<br/> | MyApp.exe<br/> |

    

     

2.  Geben Sie die Eigenschaft ein, die vom Installationsprogramm festgelegt werden soll, wenn MyApp.exe installiert ist.

    [AppSearch-Tabelle](appsearch-table.md) (partiell)

    

    | Eigenschaft         | Signatur          |
    |------------------|--------------------|
    | MyApp<br/> | Appfile<br/> |

    

     

3.  Verwenden Sie die [drlocator-Tabelle](drlocator-table.md). Geben Sie im Feld Pfad den vollständigen Pfad zur Datei auf dem Benutzersystem ein. Geben Sie in der Spalte Tiefe den Wert 0 ein, um den Ordner bin zu durchsuchen.

    [Drlocator-Tabelle](drlocator-table.md)

    

    | Signatur          | Parent | Pfad                                                    | Tiefe        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | Appfile<br/> |        | C: \\ Programmdateien \\ myProducts- \\ Projekte \\ bin<br/> | 0<br/> |

    

     

4.  Fügen Sie die Aktion AppSearch in die Aktions Sequenz ein. Wenn MyApp.exe im Ordner "C: \\ Programme \\ myProducts Projects" installiert ist \\ \\ , legt das Installationsprogramm die Eigenschaft "MyApp" auf den Speicherort der Datei fest.

 

 




