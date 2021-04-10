---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 23 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 8219f157-585d-4733-8e10-c05813b398ba
title: Benutzerdefinierter Aktionstyp 23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05576c44ab634dc117501a89e6b86594f5483458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869252"
---
# <a name="custom-action-type-23"></a>Benutzerdefinierter Aktionstyp 23

Der benutzerdefinierte Aktionstyp 23 wird bei gleichzeitigen Installationen verwendet. Parallele Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die öffentliche Veröffentlichung vorgesehen sind. Weitere Informationen zu gleichzeitigen Installationen finden Sie unter [parallele Installationen](concurrent-installations.md).

Durch diese benutzerdefinierte Aktion wird ein weiteres Installer-Paket installiert, das sich in der Quell Struktur der Anwendung befindet.

## <a name="source"></a>`Source`

Der Speicherort des gleichzeitigen Installationspakets wird relativ zum Stamm des Quell Speicher Orts angegeben, der im Quellfeld der [Tabelle "CustomAction](customaction-table.md)" angezeigt wird.

## <a name="numeric-type"></a>Numerischer Typ



| Typname                                                      | Wert |
|----------------------------------------------------------------|-------|
| msidbcustomaktiontypeinstall + msidbcustomaktionsesourcefile | 23    |



 

## <a name="target"></a>Ziel

Das Zielfeld der [Tabelle "CustomAction](customaction-table.md) " enthält Eigenschaften Einstellungen, die an die parallele Installation übermittelt werden sollen. Diese Eigenschafts Einstellungen können Funktionen angeben.

## <a name="return-processing-options"></a>Rückgabe Verarbeitungsoptionen

Die Sitzung für die gleichzeitige Installation wird im aktuellen Prozess als separater Thread ausgeführt. Eine parallele Installation kann nicht asynchron ausgeführt werden.

Weitere Informationen finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".

## <a name="execution-scheduling-options"></a>Ausführungszeit Planungsoptionen

Options-Flags sind verfügbar, um die potenzielle mehrfache Ausführung von benutzerdefinierten Aktionen zu steuern. Weitere Informationen finden Sie unter [Optionen für die Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Ausführungs Optionen für In-Script

Nicht verwendet.

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
</dt> <dt>

[Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md)
</dt> </dl>

 

 



