---
description: Die Umgebungs Tabelle wird verwendet, um die Werte von Umgebungsvariablen festzulegen.
ms.assetid: f7106ed6-706f-4e57-989f-030066bcecd3
title: Umgebungs Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a4db2e33c01685bdc40475f659e1b03b69b6c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360017"
---
# <a name="environment-table"></a>Umgebungs Tabelle

Die Umgebungs Tabelle wird verwendet, um die Werte von Umgebungsvariablen festzulegen.

Die Umgebungs Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Umgebung | [Bezeichner](identifier.md) | J   | N        |
| Name        | [Text](text.md)             | N   | N        |
| Wert       | [Großformatige](formatted.md)   | N   | J        |
| Komponente\_ | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Environment"></span><span id="environment"></span><span id="ENVIRONMENT"></span>Umgebung
</dt> <dd>

Dies ist der Primärschlüssel der Tabelle und ein nicht lokalisiertes Token.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Diese Spalte ist der lokalisierbare Name der Umgebungsvariablen. Die Schlüsselwerte werden geschrieben oder entfernt, je nachdem, welcher der Zeichen in der folgenden Tabelle dem Namen vorangestellt wird. Es gibt keine Auswirkung auf die Reihenfolge der Symbole, die in einem Präfix verwendet werden.



| Präfix                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =                              | Erstellen Sie die Umgebungsvariable, wenn Sie nicht vorhanden ist, und legen Sie Sie während der Installation fest. Wenn die Umgebungsvariable vorhanden ist, legen Sie Sie während der Installation fest.                                                                                                                                                                                                                                                                                                                                   |
| \+                             | Erstellen Sie die Umgebungsvariable, wenn Sie nicht vorhanden ist, und legen Sie Sie während der Installation fest. Dies hat keine Auswirkung auf den Wert der Umgebungsvariablen, wenn Sie bereits vorhanden ist.                                                                                                                                                                                                                                                                                                                         |
| \-                             | Entfernen Sie die Umgebungsvariable, wenn die Komponente entfernt wird. Dieses Symbol kann mit einem beliebigen Präfix kombiniert werden.                                                                                                                                                                                                                                                                                                                                                                                      |
| !                              | Entfernen Sie die Umgebungsvariable während einer Installation. Der Installer entfernt während einer Installation nur eine Umgebungsvariable, wenn der Name und der Wert der Variablen den Einträgen in den Feldern Name und Wert der Umgebungs Tabelle entsprechen. Wenn Sie eine Umgebungsvariable unabhängig von ihrem Wert entfernen möchten, verwenden Sie die Syntax "!", und lassen Sie das Feld "Wert" leer.                                                                                                                    |
| \*                             | Dieses Präfix wird mit Windows 2000 verwendet, um anzugeben, dass der Name auf eine System Umgebungsvariable verweist. Wenn kein Sternchen vorhanden ist, schreibt das Installationsprogramm die Variable in die Benutzerumgebung. Dieses Symbol kann mit einem beliebigen Präfix kombiniert werden. Ein Paket, das für die Installation im computerspezifischen [Installations Kontext](installation-context.md) verwendet wird, sollte Umgebungsvariablen in die Umgebung des Computers schreiben, indem \* in die Spalte Name eingeschlossen wird. Weitere Informationen finden Sie in den Hinweisen. |
| =-                             | Die Umgebungsvariable wird bei der Deinstallation auf Installieren und entfernen festgelegt. Dies ist das übliche Verhalten.                                                                                                                                                                                                                                                                                                                                                                                                 |
| !-                             | Entfernt während einer Installation oder Deinstallation eine Umgebungsvariable.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| =+ !+<br/> !=<br/> | Dabei handelt es sich nicht um gültige Präfixe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

Wenn das Wertfeld in der Tabelle eine enthält \[ ~ \] , gelten die Präfix Zeichen nur für den angegebenen Teil der Zeichenfolge. Die Verwendung von \[ ~ \] wird im Abschnitt Wert Spalte unten beschrieben.

Die Umgebungsvariable wird entfernt, wenn das Wertfeld der Tabelle leer ist. Daher wird bei einem leeren im Wertfeld ein =-Präfix die Umgebungsvariable bei der Installation gelöscht, und ein-Präfix löscht alle aktuellen Werte bei der Deinstallation.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Diese Spalte enthält den lokalisierbaren Wert, der als formatierte Zeichenfolge festgelegt werden soll. Siehe [formatiert](formatted.md). Wenn dieses Feld leer bleibt, wird die Variable entfernt. Wenn das Feld leer ist und der Zeichenfolge im Feld Name das Präfix-Symbol vorangestellt wird, wird die Variable nur entfernt, wenn die Komponente entfernt wird.

Um einen Wert an das Ende einer vorhandenen Variablen anzufügen, stellen Sie die Zeichenfolge in diesem Feld durch das NULL \[ ~ \] -Zeichen und das Trennzeichen als Präfix voran. Wenn z. b. das Semikolon das gewählte Trennzeichen ist: \[ ~ \] ;*Wert*.

Um dem Vordergrund einer vorhandenen Variablen einen Wert als Präfix hinzufügen, fügen Sie die Zeichenfolge in diesem Feld durch das Trennzeichen und das NULL Zeichen an \[ ~ \] . Wenn z. b. das Semikolon das ausgewählte Trennzeichen ist: *Wert*; \[ ~ \] .

Wenn kein \[ ~ \] im Feld vorhanden ist, stellt die Zeichenfolge den gesamten Wert dar, der festgelegt oder gelöscht werden soll.

Jede Zeile darf nur einen Wert enthalten. Beispielsweise der Einstiegs *Wert*; *Wert* \[ ~ ; \] ist mehr als ein Wert und sollte nicht verwendet werden, da dies zu unvorhersehbaren Ergebnissen führt. Der Einstiegs *Wert*. \[ ~ \] ist nur ein Wert.

Wenn Name das Präfix + hat, \[ ~ \] darf nicht in der Wert Spalte verwendet werden. Dies liegt daran, dass die Bedeutung von "+" und " \[ ~ \] " klar voneinander exklusiv sind.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Ein externer Schlüssel für die erste Spalte der [Komponenten Tabelle](component-table.md). Diese Spalte verweist auf die Komponente, die die Installation der Umgebungs Werte steuert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Damit das Installationsprogramm Umgebungsvariablen festlegen kann, müssen die Aktionen "Schreiben von [Schreib Aktionen](writeenvironmentstrings-action.md) " und " [removeenvironment Strings](removeenvironmentstrings-action.md) " in der [Tabelle "InstallExecuteSequence](installexecutesequence-table.md)" aufgeführt werden.

Beachten Sie, dass die Umgebungsvariablen für die laufende Installation nicht geändert werden, wenn entweder die Aktion "Schreiben von [Schreib Aktionen](writeenvironmentstrings-action.md) " oder " [removeenvironment Strings](removeenvironmentstrings-action.md) " ausgeführt wird. Unter Windows 2000 werden diese Informationen in der Registrierung gespeichert, und eine Meldung benachrichtigt das System über Änderungen, wenn die Installation abgeschlossen ist. Ein neuer Prozess oder ein anderer Prozess, der Nachrichten prüft, verwendet die neuen Umgebungsvariablen.

Wenn Sie die PATH-Umgebungsvariable mit der Umgebungs Tabelle ändern, versuchen Sie nicht, den gesamten neuen Pfad explizit in das Wertfeld einzugeben. Erweitern Sie stattdessen den vorhandenen Pfad, indem Sie einen Wert und ein Trennzeichen (;) an \[ ~ \] . Wenn \[ ~ \] nicht im Feld Wert vorhanden ist, gehen die vorhandenen Pfadinformationen verloren, und durch die Installation der MSI-Datei kann der Computer nicht gestartet werden. Die PATH-Variable wird meistens mit der folgenden Syntax festgelegt: \[ ~ \] ; Wert.

Bei der Durchführung von computerspezifischen Installationen von einem Terminal Server schreibt der Installer Umgebungsvariablen pro Benutzer in **HKU \\ . Standard \\ Umgebung**. Da Terminal Dienste diesen Abschnitt der Registrierung nicht replizieren, werden die Umgebungsvariablen pro Benutzer von der Installation nicht festgelegt. Ein Paket, das für Installationen pro Computer verwendet wird, sollte Umgebungsvariablen in die Computerumgebung schreiben, indem es \* in die Spalte Name eingeschlossen wird. Wenn das Paket pro Benutzer oder pro Computer installiert werden kann, erstellen Sie zwei Komponenten: (1) eine Einzelbenutzer Komponente mit den Umgebungs Tabellen Einträgen, die für die Benutzereinstellungen erstellt wurden, und (2) eine Computer spezifische Komponente mit der Umgebungs Tabelle, die für Computereinstellungen erstellt wurde. Bedingung: die Installation dieser Komponente wird mithilfe der Eigenschaft [**privilegiert**](privileged.md) .

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE65](ice65.md)  
[ICE69](ice69.md)  
[ICE80](ice80.md)  
</dl>

 

 




