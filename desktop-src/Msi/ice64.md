---
description: ICE64 prüft, ob neue Verzeichnisse im Benutzerprofil in roamingszenarios ordnungsgemäß entfernt werden.
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529585"
---
# <a name="ice64"></a>ICE64

ICE64 prüft, ob neue Verzeichnisse im Benutzerprofil in roamingszenarios ordnungsgemäß entfernt werden.

Wenn eine Warnung oder ein Fehler, der von ICE64 gemeldet wird, nicht behoben wird, führt dies im Allgemeinen zu Problemen bei der vollständigen Bereinigung des Computers während einer Wenn ein Roamingbenutzer, der die Anwendung installiert hat, sich zum ersten Mal bei einem Computer anmeldet, wird das gesamte Profil auf den Computer kopiert. Bei einer Ankündigung (die nach dem Download des roamingprofils erfolgt) überprüft das Installationsprogramm, ob das Verzeichnis bereits vorhanden ist, und löscht es daher bei der Installation nicht. Dadurch bleibt das Verzeichnis dauerhaft auf dem Computer des Benutzers.

## <a name="result"></a>Ergebnis

ICE64 gibt eine Warnung oder einen Fehler in einer roamingsituation aus, wenn ein neues Verzeichnis im Benutzerprofil, das entfernt werden soll, nicht entfernt wird.

## <a name="example"></a>Beispiel

ICE64 meldet den folgenden Fehler für das gezeigte Beispiel.

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

Der Ordner "myotherfolder" ist ein benutzerdefinierter Profilordner. Da es nicht in der Tabelle "RemoveFile" aufgeführt ist, wird es in einigen Szenarios nicht entfernt.

Um diesen Fehler zu beheben, erstellen Sie eine Zeile für den Ordner in der Tabelle "RemoveFile".

[Verzeichnis Tabelle](directory-table.md)



| Verzeichnis     | Über \_ geordnetes Verzeichnis | DefaultDir  |
|---------------|-------------------|-------------|
| AppDataFolder | TARGETDIR         |             |
| MyFolder      | AppDataFolder     | DataFolder  |
| Myotherfolder | AppDataFolder     | DataFolder2 |



 

[RemoveFile-Tabelle](removefile-table.md)



| Filekey | Komponente\_ | FileName | Dirproperty | InstallMode |
|---------|-------------|----------|-------------|-------------|
| Key1    | Component1  |          | MyFolder    | 2           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



