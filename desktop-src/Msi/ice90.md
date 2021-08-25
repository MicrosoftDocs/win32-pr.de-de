---
description: ICE90 gibt eine Warnung aus, wenn ermittelt wird, dass das Verzeichnis einer Verknüpfung als öffentliche Eigenschaft angegeben wurde.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fba38ba074bf939431f497e8aab73ec0640d7bbc66fb0998498ce190d99fd92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894950"
---
# <a name="ice90"></a>ICE90

ICE90 gibt eine Warnung aus, wenn ermittelt wird, dass das Verzeichnis einer Verknüpfung als öffentliche Eigenschaft angegeben wurde. Die Namen der [öffentlichen Eigenschaften](public-properties.md) werden in Großbuchstaben geschrieben. Eine von einer öffentlichen Eigenschaft angegebene Verknüpfung funktioniert möglicherweise nicht, wenn sich der Wert der [**ALLUSERS-Eigenschaft**](allusers.md) ändert.

Diese benutzerdefinierte ICE-Aktion überprüft die Verknüpfungstabelle und verwendet die Directory-Tabelle. Wenn die Directory-Tabelle nicht vorhanden ist, wird sie ohne Validierung der Verknüpfungstabelle zurückgegeben und gibt keine Fehler oder Warnungen aus.

## <a name="result"></a>Ergebnis

ICE90 gibt die folgende Warnung aus.



| ICE90-Fehler                                                                                                                                                                                                                    | BESCHREIBUNG                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Die Verknüpfung "1" verfügt über ein Verzeichnis, das eine öffentliche Eigenschaft (ALL CAPS) ist und \[ sich unter dem \] Benutzerprofilverzeichnis befindet. Dies führt zu einem Problem, wenn sich der Wert der [**ALLUSERS-Eigenschaft**](allusers.md) in der Sequenz der Benutzeroberfläche ändert. | Das Verzeichnis einer Verknüpfung wurde als öffentliche Eigenschaft angegeben. |



 

## <a name="example"></a>Beispiel

ICE90 meldet die folgende Warnung für das Beispiel:

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

In diesem Beispiel befindet sich MYDIR unter einem Benutzerprofil. ICE90 gibt eine Warnung aus, da der Speicherort des Zielverzeichnisses durch die öffentliche Eigenschaft MYDIR angegeben wird. Ein Benutzer kann die MyDIR- oder [**ALLUSERS-Eigenschaft**](allusers.md) ändern. Wenn **ALLUSERS** für den Installationskontext pro Computer festgelegt ist und MYDIR sich unter einem Benutzerprofil befindet, wird die Verknüpfungsdatei in MYDIR unter das Profil "Alle Benutzer" und nicht unter das Profil eines bestimmten Benutzers kopiert. [](installation-context.md) Wenn **ALLUSERS** für den Benutzerinstallationskontext festgelegt ist, wird die Verknüpfungsdatei in MYDIR in das Profil eines bestimmten Benutzers kopiert und ist für andere Benutzer nicht verfügbar.

[Verknüpfungstabelle](shortcut-table.md) (partiell)



| Verknüpfung  | Verzeichnis\_ |
|-----------|-------------|
| Shortcut1 | MYDIR       |



 

[Verzeichnistabelle](directory-table.md) (partiell)



| Verzeichnis | Übergeordnetes Verzeichnis \_ |
|-----------|-------------------|
| MYDIR     | ProgramMenuFolder |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



