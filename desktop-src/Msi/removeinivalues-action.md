---
description: Die RemoveIniValues-Aktion entfernt die zum Entfernen angegebenen ini-Dateiinformationen in der removeinifile-Tabelle, wenn die Komponente für die lokale Installation oder die Ausführung aus der Quelle festgelegt ist.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: RemoveIniValues-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dfb847d911e847de00ede6eab30ac3a86615eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960757"
---
# <a name="removeinivalues-action"></a>RemoveIniValues-Aktion

Die RemoveIniValues-Aktion entfernt die zum Entfernen angegebenen ini-Dateiinformationen in der [removeinifile-Tabelle](removeinifile-table.md) , wenn die Komponente für die lokale Installation oder die Ausführung aus der Quelle festgelegt ist. Die RemoveIniValues-Aktion entfernt ini-Dateiinformationen, die einer Komponente in der Tabelle " [IniFile](inifile-table.md)" zugeordnet wurden. Mit dieser Aktion werden auch ini-Dateiinformationen entfernt, wenn die Informationen von der [Aktion "Write-einivalues](writeinivalues-action.md) " geschrieben und die Komponente deinstalliert werden soll.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die [InstallValidate](installvalidate-action.md) -Aktion muss vor der RemoveIniValues-Aktion aufgerufen werden. Wenn eine " [Write](writeinivalues-action.md) "-Aktion in der Sequenz verwendet wird, muss Sie nach "RemoveIniValues" angezeigt werden.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten    |
|-------|-------------------------------|
| \[1\] | Bezeichner der INI-Datei.      |
| \[2\] | Der Schlüssel Abschnitt der INI-Datei.     |
| \[3\] | Das Element wurde aus der INI-Datei entfernt.  |
| \[4\] | Der Wert wurde aus der INI-Datei entfernt. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Removeinifile-Tabelle](removeinifile-table.md)
</dt> <dt>

[INIFILE-Tabelle](inifile-table.md)
</dt> <dt>

[Aktion "Write-einivalues"](writeinivalues-action.md)
</dt> <dt>

[InstallValidate](installvalidate-action.md)
</dt> </dl>

 

 



