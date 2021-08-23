---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 23 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 8219f157-585d-4733-8e10-c05813b398ba
title: Benutzerdefinierter Aktionstyp 23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eeeb7e1056b9644baecdc8a4e5da959ad7320c960ea1de2ad38f9868f6e4c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637874"
---
# <a name="custom-action-type-23"></a>Benutzerdefinierter Aktionstyp 23

Der benutzerdefinierte Aktionstyp 23 wird bei gleichzeitigen Installationen verwendet. Gleichzeitige Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die Veröffentlichung an die Öffentlichkeit vorgesehen sind. Informationen zu gleichzeitigen Installationen finden Sie unter [Gleichzeitige Installationen.](concurrent-installations.md)

Mit dieser benutzerdefinierten Aktion wird ein weiteres Installationspaket installiert, das sich in der Quellstruktur der Anwendung befindet.

## <a name="source"></a>Quelle

Der Speicherort des Pakets für die gleichzeitige Installation wird relativ zum Stamm des Quellspeicherorts angegeben, der im Feld Quelle der [CustomAction-Tabelle angezeigt wird.](customaction-table.md)

## <a name="numeric-type"></a>Numerischer Typ



| Typname                                                      | Wert |
|----------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeSourceFile | 23    |



 

## <a name="target"></a>Ziel

Das Feld Ziel der [CustomAction-Tabelle enthält](customaction-table.md) Eigenschafteneinstellungen, die an die gleichzeitige Installation übergeben werden sollen. Diese Eigenschafteneinstellungen können Features angeben.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Die sitzungs gleichzeitige Installation wird im aktuellen Prozess als separater Thread ausgeführt. Eine gleichzeitige Installation kann nicht asynchron ausgeführt werden.

Weitere Informationen finden Sie unter [Rückgabeverarbeitungsoptionen für benutzerdefinierte Aktionen.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Optionsflags sind verfügbar, um die potenzielle mehrfache Ausführung benutzerdefinierter Aktionen zu steuern. Weitere Informationen finden Sie unter [Optionen für die Benutzerdefinierte Aktionsausführungsplanung.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Wird nicht verwendet.

## <a name="return-values"></a>Rückgabewerte

Der Rückgabestatus des Benutzerabtritts, -fehlers, -aussetzens oder -erfolgs aus einer gleichzeitigen Installation wird auf die gleiche Weise wie jede andere Aktion verarbeitet. Beachten Sie jedoch, dass Windows Installer die Rückgabewerte aller Aktionen übersetzt, wenn der Rückgabewert in die Protokolldatei geschrieben wird. Wenn der Rückgabewert der Aktion beispielsweise in der Protokolldatei als 1 angezeigt wird, bedeutet dies, dass die Aktion ERROR SUCCESS zurückgegeben \_ hat. Weitere Informationen finden Sie unter [Protokollierung von Aktions-Rückgabewerten.](logging-of-action-return-values.md)

Wenn für eine gleichzeitige Installation **msidbCustomActionTypeContinue** festgelegt ist, wird die Rückgabe von ERROR \_ INSTALL \_ USEREXIT, ERROR \_ INSTALL \_ REBOOT, ERROR INSTALL REBOOT NOW oder ERROR SUCCESS REBOOT REQUIRED als \_ ERROR SUCCESS \_ \_ \_ \_ \_ \_ behandelt. Dies bedeutet, dass die Anforderung für den Neustart ignoriert wird, wenn Sie **msidbCustomActionTypeContinue** festlegen und ihre gleichzeitige Installation einen Neustart erfordert. Darüber hinaus wird der Fehlercode aus der benutzerdefinierten Aktion für die gleichzeitige Installation ignoriert.

Wenn **msidbCustomActionTypeContinue** nicht festgelegt ist, werden die folgenden Rückgabecodes plus ERROR SUCCESS als erfolgreich behandelt und \_ haben die folgende Bedeutung. Andere Rückgabecodes werden als Fehler behandelt.



| Nachricht                          | Bedeutung                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| FEHLER \_ BEIM NEUSTART DER \_ INSTALLATION           | Das Neustartflag wird so festgelegt, dass es am Ende der Installation neu gestartet wird.                                  |
| FEHLER: \_ \_ JETZT NEU STARTEN \_ INSTALLIEREN      | Vor Abschluss der Installation ist ein Neustart erforderlich. Der Neustart wird sofort verarbeitet. |
| FEHLER: \_ \_ NEUSTART ERFOLGREICH \_ ERFORDERLICH | Ein Neustart war erforderlich, wurde jedoch unterdrückt.                                                          |



 

## <a name="remarks"></a>Hinweise

Ein bedingter Ausdruck ist erforderlich, um die gleichzeitige Installation bei der Installation oder Entfernung der zugeordneten Komponente oder Funktion zu aktivieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gleichzeitige Installationen](concurrent-installations.md)
</dt> <dt>

[Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
</dt> <dt>

[Informationen zu benutzerdefinierten Aktionen](about-custom-actions.md)
</dt> <dt>

[Verwenden benutzerdefinierter Aktionen](using-custom-actions.md)
</dt> <dt>

[Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md)
</dt> </dl>

 

 



