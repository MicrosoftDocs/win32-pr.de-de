---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 7 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 4a8f35f9-58a8-417e-b72e-159f4af7d83f
title: Benutzerdefinierter Aktionstyp 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6735546b4db55bc8f9875fa2cd267eb0877a52c92e0a0073a942165dc413055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947911"
---
# <a name="custom-action-type-7"></a>Benutzerdefinierter Aktionstyp 7

Der benutzerdefinierte Aktionstyp 7 wird mit gleichzeitigen Installationen verwendet. Gleichzeitige Installationen werden für die Installation von Anwendungen, die für die Veröffentlichung in der Öffentlichkeit vorgesehen sind, nicht empfohlen. Weitere Informationen zu gleichzeitigen Installationen finden Sie unter [Gleichzeitige Installationen.](concurrent-installations.md)

Diese benutzerdefinierte Aktion installiert ein anderes Installationspaket, das innerhalb des ersten Pakets geschachtelt ist.

## <a name="source"></a>`Source`

Die Datenbank der gleichzeitigen Anwendung wird als Unterspeicher des Pakets gespeichert, und der Name des Unterspeichers wird im Feld Quelle der [CustomAction-Tabelle](customaction-table.md)festgelegt.

## <a name="numeric-type"></a>Numerischer Typ



| Typname                                                      | Wert |
|----------------------------------------------------------------|-------|
| msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData | 7     |



 

## <a name="target"></a>Ziel

Das Feld Target der [Tabelle CustomAction](customaction-table.md) enthält Eigenschafteneinstellungen, die an die gleichzeitige Installation übergeben werden sollen. Diese Eigenschafteneinstellungen können Features angeben.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Die gleichzeitige Installationssitzung wird im aktuellen Prozess als separater Thread ausgeführt. Eine gleichzeitige Installation kann nicht asynchron ausgeführt werden.

Weitere Informationen finden Sie unter [Rückgabeverarbeitungsoptionen für benutzerdefinierte Aktionen.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Optionsflags sind verfügbar, um die potenzielle Mehrfachausführung benutzerdefinierter Aktionen zu steuern. Weitere Informationen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Diese Option wird von dieser benutzerdefinierten Aktion nicht verwendet.

## <a name="return-values"></a>Rückgabewerte

Der Rückgabestatus von Benutzerabbruch, Fehler, Anhalten oder Erfolg einer gleichzeitigen Installation wird auf die gleiche Weise wie jede andere Aktion verarbeitet. Beachten Sie jedoch, dass Windows Installer die Rückgabewerte aus allen Aktionen übersetzt, wenn der Rückgabewert in die Protokolldatei geschrieben wird. Wenn beispielsweise der Rückgabewert der Aktion in der Protokolldatei als 1 angezeigt wird, bedeutet dies, dass die Aktion ERROR SUCCESS zurückgegeben \_ hat. Weitere Informationen zu dieser Übersetzung finden Sie unter [Protokollierung von Aktionsrückgabewerten.](logging-of-action-return-values.md)

Beachten Sie Folgendes: Wenn für eine gleichzeitige Installation **msidbCustomActionTypeContinue** festgelegt ist, wird eine Rückgabe von ERROR \_ INSTALL \_ USEREXIT, ERROR \_ INSTALL \_ REBOOT, ERROR INSTALL REBOOT \_ NOW oder ERROR SUCCESS REBOOT REQUIRED als FEHLER ERFOLGREICH \_ \_ \_ \_ \_ \_ behandelt. Dies bedeutet, dass die Anforderung für den Neustart ignoriert wird, wenn Sie **msidbCustomActionTypeContinue** festlegen und die gleichzeitige Installation einen Neustart erfordert. Darüber hinaus wird der Fehlercode aus der benutzerdefinierten Aktion für die gleichzeitige Installation ignoriert.

Wenn **msidbCustomActionTypeContinue** nicht festgelegt ist, werden die folgenden Rückgabecodes plus ERROR \_ SUCCESS als erfolg behandelt und haben die folgende Bedeutung. Andere Rückgabecodes werden als Fehler behandelt.



| Nachricht                          | Bedeutung                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| FEHLER BEIM \_ NEUSTART DER INSTALLATION \_           | Das Neustartflag wird so festgelegt, dass es am Ende der Installation neu gestartet wird.                                  |
| FEHLER " \_ \_ JETZT NEU STARTEN INSTALLIEREN" \_      | Vor Abschluss der Installation ist ein Neustart erforderlich. Der Neustart wird sofort verarbeitet. |
| FEHLER \_ BEI \_ ERFOLGREICHEM NEUSTART \_ ERFORDERLICH | Ein Neustart war erforderlich, wurde jedoch unterdrückt.                                                          |



 

## <a name="remarks"></a>Hinweise

Ein bedingter Ausdruck ist erforderlich, um die gleichzeitige Installation entweder bei der Installation oder beim Entfernen der zugeordneten Komponente oder Funktion zu aktivieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gleichzeitige Installationen](concurrent-installations.md)
</dt> <dt>

[Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
</dt> <dt>

[Informationen zu benutzerdefinierten Aktionen](about-custom-actions.md)
</dt> <dt>

[Verwenden von benutzerdefinierten Aktionen](using-custom-actions.md)
</dt> <dt>

[Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md)
</dt> </dl>

 

 



