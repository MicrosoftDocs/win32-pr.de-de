---
description: Während einer installation Windows Installers kann das Installationsprogramm an einem bestimmten Speicherort auf dem System des Benutzers nach einer Datei suchen.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Suchen nach einer Datei an einem bestimmten Speicherort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b131708e5f9ff37474864aa5d6ef13abcab8f0d162563ca810c7e31fe2c41c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041150"
---
# <a name="searching-for-a-file-in-a-specific-location"></a>Suchen nach einer Datei an einem bestimmten Speicherort

**So suchen Sie nach einer Datei an einem bestimmten Speicherort auf einem Benutzersystem**

1.  Listen Sie die Dateisignatur und den Namen in der [Signaturtabelle auf.](signature-table.md) Die verbleibenden Felder in diesem Datensatz können NULL sein, um nach einer beliebigen Version von MyApp.exe zu suchen.

    [Signaturtabelle](signature-table.md)

    

    | Signatur          | Dateiname            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Geben Sie die Eigenschaft ein, die der Installer festlegen soll, wenn MyApp.exe installiert ist.

    [AppSearch-Tabelle](appsearch-table.md) (partiell)

    

    | Eigenschaft         | Signatur          |
    |------------------|--------------------|
    | Myapp<br/> | AppFile<br/> |

    

     

3.  Verwenden Sie die [DrLocator-Tabelle](drlocator-table.md). Geben Sie im Feld Pfad den vollständigen Pfad zur Datei auf dem Benutzersystem ein. Geben Sie in der Spalte Tiefe den Wert 0 ein, um den Ordner bin zu durchsuchen.

    [DrLocator-Tabelle](drlocator-table.md)

    

    | Signatur          | Parent | Pfad                                                    | Tiefe        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | AppFile<br/> |        | C: \\ Programme \\ MyProducts \\ Projects \\ bin<br/> | 0<br/> |

    

     

4.  Schließen Sie die AppSearch-Aktion in die Aktionssequenz ein. Wenn MyApp.exe in der Datei C: \\ Programme \\ MyProducts Projects installiert \\ \\ ist, legt der Installer die Eigenschaft MYAPP auf den Speicherort der Datei fest.

 

 




