---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 39 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: edf96cc6-ef32-4660-b4ee-50c130626e15
title: Benutzerdefinierter Aktionstyp 39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49667fbad6e71aa8b2197b00ae9dd49f7dfff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866091"
---
# <a name="custom-action-type-39"></a>Benutzerdefinierter Aktionstyp 39

Der benutzerdefinierte Aktionstyp 39 wird bei gleichzeitigen Installationen verwendet. Parallele Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die öffentliche Veröffentlichung vorgesehen sind. Weitere Informationen zu gleichzeitigen Installationen finden Sie unter [parallele Installationen](concurrent-installations.md).

Typ 39 benutzerdefinierte Aktion installiert eine Anwendung, die angekündigt oder bereits installiert ist. Dieser benutzerdefinierte Aktionstyp kann verwendet werden, um ein Produkt, das vom Installationspaket des aktuellen Produkts als gleichzeitige Installation installiert wurde, neu zu installieren oder zu entfernen. Die benutzerdefinierte Aktion vom Typ 39 kann nicht zum erneuten Installieren oder Entfernen eines Produkts verwendet werden, das zuvor auf andere Weise installiert wurde. Wenn das sekundäre Produkt z. b. mithilfe des Typs 39, Typ 23 oder benutzerdefinierte Aktion 7 bei der Installation des primären Produkts installiert wird, kann eine benutzerdefinierte Aktion vom Typ 39 verwendet werden, um das sekundäre Produkt zu entfernen, wenn das primäre Produkt deinstalliert wird.

## <a name="source"></a>`Source`

Das Feld "Source" der [Tabelle "CustomAction](customaction-table.md) " enthält den Produktcode für die Anwendung.

## <a name="numeric-type"></a>Numerischer Typ



| Typname                                                     | Wert |
|---------------------------------------------------------------|-------|
| msidbcustomaktiontypeingestall + msidbcustomaktiontypedirectory | 39    |



 

## <a name="target"></a>Ziel

Das Zielfeld der [Tabelle "CustomAction](customaction-table.md) " enthält Eigenschaften Einstellungen, die an die parallele Installation übermittelt werden sollen. Diese Eigenschafts Einstellungen können Funktionen angeben.

## <a name="return-processing-options"></a>Rückgabe Verarbeitungsoptionen

Der benutzerdefinierte Aktionstyp 39 schlägt fehl, wenn die Anwendung nicht angekündigt oder installiert wird. Um diesen Fehler zu vermeiden, müssen Sie **msidbcustomaktiontypecontinueflag** festlegen.

Eine parallele Installation kann nicht asynchron ausgeführt werden.

Weitere Informationen finden Sie unter [benutzerdefinierte Aktion Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Ausführungszeit Planungsoptionen

Options-Flags sind verfügbar, um die potenzielle mehrfache Ausführung von benutzerdefinierten Aktionen zu steuern. Siehe [Optionen für die Ausführung von benutzerdefinierten Aktionen](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Ausführungs Optionen für In-Script

Diese Option wird von der benutzerdefinierten Aktion nicht verwendet.

## <a name="return-values"></a>Rückgabewerte

Der Rückgabestatus von "Benutzer beenden", "Fehler", "aussetzen" oder "Erfolg" von einer gleichzeitigen Installation wird auf die gleiche Weise wie jede andere Aktion verarbeitet. Beachten Sie jedoch, dass Windows Installer die Rückgabewerte aller Aktionen übersetzt, wenn der Rückgabewert in die Protokolldatei geschrieben wird. Wenn der Rückgabewert der Aktion z. b. als 1 in der Protokolldatei angezeigt wird, bedeutet dies, dass die Aktion Fehler erfolgreich zurückgegeben hat \_ . Weitere Informationen finden Sie unter [Protokollieren von Aktions Rückgabe Werten](logging-of-action-return-values.md).

Beachten Sie Folgendes: Wenn für eine parallele Installation **msidbcustomaktiontypecontinue** festgelegt ist, wird bei der Rückgabe des Fehlers "UserExit installieren", "Fehler Installation neu starten", " \_ \_ \_ \_ Fehler \_ Installation \_ jetzt starten" \_ oder "Fehler beim \_ \_ Neustart \_ erforderlich" als Fehler \_ Erfolg behandelt. Dies bedeutet Folgendes: Wenn Sie **msidbcustomaktiontypecontinue** festlegen und die gleichzeitige Installation einen Neustart erfordert, wird die Anforderung für den Neustart ignoriert. Außerdem wird der Fehlercode von der benutzerdefinierten Aktion für die gleichzeitige Installation ignoriert.

Wenn **msidbcustomaktiontypecontinue** nicht festgelegt ist, werden die folgenden Rückgabecodes zuzüglich Fehler \_ Erfolg als Erfolg behandelt und haben die folgenden Bedeutungen. Andere Rückgabecodes werden als Fehler behandelt.



| Nachricht                          | Bedeutung                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| Fehler beim \_ Installieren des \_ Starts           | Das Flag für das Neustart wird am Ende der Installation auf neu starten festgelegt.                                  |
| Fehler beim \_ Installieren des \_ Neustarts. \_      | Vor Abschluss der Installation ist ein Neustart erforderlich. Der Neustart wird sofort verarbeitet. |
| Fehler \_ beim \_ Neustart \_ erforderlich. | Ein Neustart war erforderlich, wurde jedoch unterdrückt.                                                          |



 

## <a name="remarks"></a>Bemerkungen

Ein bedingter Ausdruck ist erforderlich, um die gleichzeitige Installation bei Installation oder Entfernung der zugeordneten Komponente oder Funktion zu aktivieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Parallele Installationen](concurrent-installations.md)
</dt> <dt>

[Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
</dt> <dt>

[Informationen zu benutzerdefinierten Aktionen](about-custom-actions.md)
</dt> <dt>

[Verwenden von benutzerdefinierten Aktionen](using-custom-actions.md)
</dt> </dl>

 

 



