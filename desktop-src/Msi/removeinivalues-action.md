---
description: Die RemoveIniValues-Aktion entfernt .ini Dateiinformationen, die zum Entfernen in der RemoveIniFile-Tabelle angegeben sind, wenn die Komponente so festgelegt ist, dass sie lokal installiert oder aus der Quelle ausgeführt wird.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: RemoveIniValues-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095985165bf6d9629aa0cae67a5b3f7975d817151ac4b04de40a08d5c2bab4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626389"
---
# <a name="removeinivalues-action"></a>RemoveIniValues-Aktion

Die RemoveIniValues-Aktion entfernt .ini, die zum Entfernen in der [RemoveIniFile-Tabelle](removeinifile-table.md) angegeben sind, wenn die Komponente so festgelegt ist, dass sie lokal installiert oder aus der Quelle ausgeführt wird. Die RemoveIniValues-Aktion entfernt .ini Dateiinformationen, die einer Komponente in der [IniFile-Tabelle zugeordnet wurden.](inifile-table.md) Diese Aktion entfernt auch .ini Dateiinformationen, wenn die Informationen von der [WriteIniValues-Aktion](writeinivalues-action.md) geschrieben wurden und die Deinstallation der Komponente geplant ist.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die [InstallValidate-Aktion](installvalidate-action.md) muss vor der RemoveIniValues-Aktion aufgerufen werden. Wenn eine [WriteIniValues-Aktion](writeinivalues-action.md) in der Sequenz verwendet wird, muss sie nach RemoveIniValues angezeigt werden.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten    |
|-------|-------------------------------|
| \[1\] | Bezeichner .ini Datei.      |
| \[2\] | Ein .ini Dateischlüsselabschnitt.     |
| \[3\] | Aus der .ini entferntes Element.  |
| \[4\] | Aus der .ini entfernter Wert. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[RemoveIniFile-Tabelle](removeinifile-table.md)
</dt> <dt>

[IniFile-Tabelle](inifile-table.md)
</dt> <dt>

[WriteIniValues-Aktion](writeinivalues-action.md)
</dt> <dt>

[InstallValidate](installvalidate-action.md)
</dt> </dl>

 

 



