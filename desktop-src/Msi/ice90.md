---
description: ICE90 gibt eine Warnung aus, wenn feststellt, dass das Verzeichnis einer Verknüpfung als öffentliche Eigenschaft angegeben wurde.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b4063d06aa5a0a8688e2a411040d4b64f58f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864224"
---
# <a name="ice90"></a>ICE90

ICE90 gibt eine Warnung aus, wenn feststellt, dass das Verzeichnis einer Verknüpfung als öffentliche Eigenschaft angegeben wurde. Die Namen [öffentlicher Eigenschaften](public-properties.md) werden in Großbuchstaben geschrieben. Eine von einer öffentlichen Eigenschaft angegebene Verknüpfung funktioniert möglicherweise nicht, wenn sich der Wert der [**ALLUSERS**](allusers.md) -Eigenschaft ändert.

Diese benutzerdefinierte Ice-Aktion überprüft die Verknüpfungs Tabelle und verwendet die Verzeichnis Tabelle. Wenn die Verzeichnis Tabelle nicht vorhanden ist, wird Sie ohne Überprüfung der Verknüpfungs Tabelle zurückgegeben, und es werden keine Fehler oder Warnungen ausgegeben.

## <a name="result"></a>Ergebnis

ICE90 gibt die folgende Warnung aus.



| ICE90-Fehler                                                                                                                                                                                                                    | BESCHREIBUNG                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Die Verknüpfung ' \[ 1 \] ' weist ein Verzeichnis auf, das eine öffentliche Eigenschaft (Alle Caps) und das Benutzerprofil Verzeichnis ist. Dies führt zu einem Problem, wenn der Wert der [**ALLUSERS**](allusers.md) -Eigenschaft in der UI-Sequenz geändert wird. | Das Verzeichnis einer Verknüpfung wurde als öffentliche Eigenschaft angegeben. |



 

## <a name="example"></a>Beispiel

ICE90 meldet folgende Warnung für das Beispiel:

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

In diesem Beispiel befindet sich mydir unter einem Benutzerprofil. ICE90 gibt eine Warnung aus, da der Speicherort des Zielverzeichnisses von der öffentlichen Eigenschaft mydir angegeben wird. Ein Benutzer darf die Eigenschaft mydir oder [**ALLUSERS**](allusers.md) ändern. Wenn für den [Installations Kontext](installation-context.md)pro Computer " **ALLUSERS** " festgelegt ist und sich "MyDir" unter einem Benutzerprofil befindet, wird die Verknüpfungs Datei in "MyDir" unter das Profil "alle Benutzer" und nicht auf das Profil eines bestimmten Benutzers kopiert. Wenn für den pro-Benutzer-Installations Kontext **ALLUSERS** festgelegt ist, wird die Verknüpfungs Datei in mydir in das Profil eines bestimmten Benutzers kopiert und ist für andere Benutzer nicht verfügbar.

Verknüpfungs [Tabelle](shortcut-table.md) (partiell)



| Abkürzung  | Verzeichnis\_ |
|-----------|-------------|
| Shortcut1 | "MyDir"       |



 

[Verzeichnis Tabelle](directory-table.md) (partiell)



| Verzeichnis | Über \_ geordnetes Verzeichnis |
|-----------|-------------------|
| "MyDir"     | Programmmenufolder |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



