---
description: Während einer Windows Installer-Installation kann das Installationsprogramm nach einem Verzeichnis und einer Datei in diesem Verzeichnis suchen.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Suchen nach einem Verzeichnis und einer Datei im Verzeichnis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e857460dc58fa5fded802cb53b9ae6a558e5a27426baef87be9f561fa35fe6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041180"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a>Suchen nach einem Verzeichnis und einer Datei im Verzeichnis

**So suchen Sie nach einem Verzeichnis und dann nach einer Datei in diesem Verzeichnis**

1.  Suchen Sie zunächst nach dem Verzeichnis.

    AppDir muss als gültige Signatur des Verzeichnisses definiert werden. Wenn AppDir nicht als gültige Signatur definiert ist, verfügt AppSearch nicht über einen Ort zum Suchen der Datei, z. B. wenn die Suche nach c: \\ MyDir \\MyApp.exe erfolgt, sollte AppDir als c: \\ MyDir definiert werden. AppDir kann durch Das Aufnehmen eines Datensatzes in die [DrLocator-Tabelle](drlocator-table.md)oder durch eine andere Methode definiert werden. In der Signaturtabelle ist kein [Datensatz für](signature-table.md) die Verzeichnissuche enthalten. Listen Sie für die Dateisuche die Dateisignatur und den Namen in der Signaturtabelle auf. Die verbleibenden Felder in diesem Datensatz können NULL sein, um nach einer beliebigen Version der MyApp.exe.

    [Signaturtabelle](signature-table.md) (partiell)

    

    | Signatur          | Dateiname            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  Verwenden Sie die [AppSearch-Tabelle](appsearch-table.md).

    Geben Sie die Eigenschaft ein, die der Installer festlegen soll, wenn das Verzeichnis mit der Signatur AppDir installiert ist. Wenn das Installationsprogramm findet, dass dieses Verzeichnis installiert ist, legt es MYDIR auf den Verzeichnispfad fest. Geben Sie die Eigenschaft ein, die der Installer festlegen soll, MyApp.exe installiert ist.

    [AppSearch-Tabelle](appsearch-table.md) (partiell)

    

    | Eigenschaft         | Signatur          |
    |------------------|--------------------|
    | MYDIR<br/> | AppDir<br/>  |
    | Myapp<br/> | AppFile<br/> |

    

     

3.  Verwenden Sie die [DrLocator-Tabelle](drlocator-table.md).

    Geben Sie in der Spalte Übergeordnete Spalte die Signatur AppDir ein, die als Pfad des Verzeichnisses definiert ist. Geben Sie in der Spalte Tiefe die Anzahl der Unterverzeichnisebenen an, die in diesem Verzeichnis gesucht werden soll. AppDir muss als Verzeichnissignatur definiert werden. AppDir kann durch Das Aufnehmen eines Datensatzes wie hier gezeigt oder durch eine andere Methode definiert werden.

    [DrLocator-Tabelle](drlocator-table.md)

    

    | Signatur | Parent | Pfad      | Tiefe |
    |-----------|--------|-----------|-------|
    | AppDir    |        | C: \\ MyDir | 0     |
    | AppFile   | AppDir |           | 0     |

    

     

4.  Schließen Sie die AppSearch-Aktion in die Aktionssequenz ein.

    Wenn MyApp.exe in AppDir installiert wurde, legt der Installer die Eigenschaft MYAPP auf den Speicherort der Datei fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Suchen nach vorhandenen Anwendungen, Dateien, Registrierungseinträgen oder .ini Dateieinträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




