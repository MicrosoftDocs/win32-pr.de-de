---
description: Während einer Windows Installer Installation kann das Installationsprogramm nach einem Verzeichnis und einer Datei in diesem Verzeichnis suchen.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Suchen nach einem Verzeichnis und einer Datei im Verzeichnis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4821a53ef0c3f063e943f1f5821b043791dd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348681"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a>Suchen nach einem Verzeichnis und einer Datei im Verzeichnis

**So suchen Sie nach einem Verzeichnis und dann nach einer Datei in diesem Verzeichnis**

1.  Suchen Sie zuerst nach dem Verzeichnis.

    Appdir muss als gültige Signatur des Verzeichnisses definiert werden. Wenn appdir nicht als gültige Signatur definiert ist, hat AppSearch keinen Ort, um die Datei zu finden. wenn die Suche z. b. für c: \\ mydir \\MyApp.exe ist, muss appdir als c: \\ mydir definiert werden. Appdir kann durch Einschließen eines Datensatzes in der [drlocator-Tabelle](drlocator-table.md)oder einer anderen Methode definiert werden. In der [Signatur Tabelle](signature-table.md) für die Verzeichnis Suche ist kein Datensatz enthalten. Listen Sie die Datei Signatur und den Namen der Dateisuche in der Signatur Tabelle auf. Die verbleibenden Felder in diesem Datensatz können NULL sein, um nach einer beliebigen Version von MyApp.exe zu suchen.

    [Signatur Tabelle](signature-table.md) (partiell)

    

    | Signatur          | Dateiname            |
    |--------------------|----------------------|
    | Appfile<br/> | MyApp.exe<br/> |

    

     

2.  Verwenden Sie die [AppSearch-Tabelle](appsearch-table.md).

    Geben Sie die Eigenschaft ein, die vom Installationsprogramm festgelegt werden soll, wenn das Verzeichnis mit der Signatur appdir installiert ist. Wenn das Installationsprogramm feststellt, dass dieses Verzeichnis installiert ist, wird mydir auf den Verzeichnispfad festgelegt. Geben Sie die Eigenschaft ein, die vom Installationsprogramm festgelegt werden soll, wenn MyApp.exe installiert ist.

    [AppSearch-Tabelle](appsearch-table.md) (partiell)

    

    | Eigenschaft         | Signatur          |
    |------------------|--------------------|
    | "MyDir"<br/> | AppDir<br/>  |
    | MyApp<br/> | Appfile<br/> |

    

     

3.  Verwenden Sie die [drlocator-Tabelle](drlocator-table.md).

    Geben Sie in der übergeordneten Spalte die Signatur (appdir) ein, die als Pfad des Verzeichnisses definiert ist. Geben Sie in der Spalte Tiefe die Anzahl der Unterverzeichnis Ebenen an, die in diesem Verzeichnis durchsucht werden sollen. Appdir muss als Verzeichnis Signatur definiert werden. Appdir kann durch Einschließen eines Datensatzes definiert werden, wie hier gezeigt, oder durch eine andere Methode.

    [Drlocator-Tabelle](drlocator-table.md)

    

    | Signatur | Parent | Pfad      | Tiefe |
    |-----------|--------|-----------|-------|
    | AppDir    |        | C: \\ meindir | 0     |
    | Appfile   | AppDir |           | 0     |

    

     

4.  Fügen Sie die Aktion AppSearch in die Aktions Sequenz ein.

    Wenn MyApp.exe in appdir installiert wird, legt das Installationsprogramm die Eigenschaft MyApp auf den Speicherort der Datei fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




