---
description: Die Tabelle Environment wird verwendet, um die Werte von Umgebungsvariablen festzulegen.
ms.assetid: f7106ed6-706f-4e57-989f-030066bcecd3
title: Umgebungstabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de1fe52e8222bfde3e451b6ccc543511822e0d511a2ce1ce2b6bee8bc4fd117f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129600"
---
# <a name="environment-table"></a>Umgebungstabelle

Die Tabelle Environment wird verwendet, um die Werte von Umgebungsvariablen festzulegen.

Die Tabelle Environment weist die folgenden Spalten auf.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Environment | [Identifier](identifier.md) | J   | N        |
| Name        | [Text](text.md)             | N   | N        |
| Wert       | [Formatiert](formatted.md)   | N   | J        |
| Komponente\_ | [Identifier](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Environment"></span><span id="environment"></span><span id="ENVIRONMENT"></span>Umgebung
</dt> <dd>

Dies ist der Primärschlüssel der Tabelle und ein nicht lokalisiertes Token.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Diese Spalte ist der lokalisierbare Name der Umgebungsvariablen. Die Schlüsselwerte werden geschrieben oder entfernt, je nachdem, welchen Zeichen in der folgenden Tabelle der Name vorangestellt ist. Die Reihenfolge der in einem Präfix verwendeten Symbole hat keine Auswirkungen.



| Präfix                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =                              | Erstellen Sie die Umgebungsvariable, wenn sie nicht vorhanden ist, und legen Sie sie dann während der Installation fest. Wenn die Umgebungsvariable vorhanden ist, legen Sie sie während der Installation fest.                                                                                                                                                                                                                                                                                                                                   |
| \+                             | Erstellen Sie die Umgebungsvariable, wenn sie nicht vorhanden ist, und legen Sie sie während der Installation fest. Dies hat keine Auswirkungen auf den Wert der Umgebungsvariablen, wenn sie bereits vorhanden ist.                                                                                                                                                                                                                                                                                                                         |
| \-                             | Entfernen Sie die Umgebungsvariable, wenn die Komponente entfernt wird. Dieses Symbol kann mit einem beliebigen Präfix kombiniert werden.                                                                                                                                                                                                                                                                                                                                                                                      |
| !                              | Entfernen Sie die Umgebungsvariable während einer Installation. Das Installationsprogramm entfernt während einer Installation nur dann eine Umgebungsvariable, wenn Name und Wert der Variablen mit den Einträgen in den Feldern Name und Wert der Umgebungstabelle übereinstimmen. Wenn Sie eine Umgebungsvariable unabhängig von ihrem Wert entfernen möchten, verwenden Sie die Syntax "!", und lassen Sie das Feld Wert leer.                                                                                                                    |
| \*                             | Dieses Präfix wird mit Windows 2000 verwendet, um anzugeben, dass der Name auf eine Systemumgebungsvariable verweist. Wenn kein Sternchen vorhanden ist, schreibt das Installationsprogramm die Variable in die Umgebung des Benutzers. Dieses Symbol kann mit einem beliebigen Präfix kombiniert werden. Ein Paket, das für die Installation im [Installationskontext](installation-context.md) pro Computer verwendet wird, sollte Umgebungsvariablen in die Umgebung des Computers schreiben, indem \* es in die Spalte Name eingeschlossen wird. Weitere Informationen finden Sie in den Hinweisen. |
| =-                             | Die Umgebungsvariable wird bei der Installation festgelegt und bei der Deinstallation entfernt. Dies ist das übliche Verhalten.                                                                                                                                                                                                                                                                                                                                                                                                 |
| !-                             | Entfernt eine Umgebungsvariable während einer Installation oder Deinstallation.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| =+ !+<br/> !=<br/> | Dies sind keine gültigen Präfixe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

Wenn das Feld Wert in der Tabelle ein \[ ~ \] enthält, gelten die Präfixzeichen nur für den angegebenen Teil der Zeichenfolge. Die Verwendung von \[ ~ \] wird unten im Abschnitt Wertspalte beschrieben.

Die Umgebungsvariable wird entfernt, wenn das Feld Wert der Tabelle leer ist. Daher löscht ein = -Präfix mit einem leerzeichen im Feld Wert die Umgebungsvariable bei der Installation, und ein -Präfix löscht alle aktuellen Werte bei der Deinstallation.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert
</dt> <dd>

Diese Spalte enthält den lokalisierbaren Wert, der als formatierte Zeichenfolge festgelegt werden soll. Weitere Informationen finden Sie unter [Formatiertes](formatted.md). Wenn dieses Feld leer gelassen wird, wird die Variable entfernt. Wenn das Feld leer ist und der Zeichenfolge im Feld Name das -Symbol vorangestellt ist, wird die Variable nur entfernt, wenn die Komponente entfernt wird.

Um einen Wert an das Ende einer vorhandenen Variablen anzufügen, stellen Sie der Zeichenfolge in diesem Feld das Nullzeichen \[ ~ \] und das Trennzeichen voran. Wenn das Semikolon beispielsweise das ausgewählte Trennzeichen ist: \[ ~ \] ;*Der Wert*.

Fügen Sie die Zeichenfolge in diesem Feld durch das Trennzeichen und das Nullzeichen an, um einen Wert vor einer vorhandenen Variablen zu \[ ~ \] setzen. Wenn das Semikolon beispielsweise das ausgewählte Trennzeichen ist: *Wert*; \[ ~ \] .

Wenn im Feld kein \[ ~ \] vorhanden ist, stellt die Zeichenfolge den gesamten festzulegenden oder zu löschenden Wert dar.

Jede Zeile kann nur einen Wert enthalten. Beispiel: der Eintrag *Wert*; *Wert*; \[ ~ \] ist mehr als ein Wert und sollte nicht verwendet werden, da er unvorhersehbare Ergebnisse verursacht. Der Eintrag *Wert*; \[ ~ \] ist nur ein Wert.

Wenn Name das Präfix +hat, \[ ~ \] darf nicht in der Spalte Wert verwendet werden. Dies liegt daran, dass die Bedeutung von "+" und \[ ~ \] "" eindeutig voneinander ausschließen.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Ein externer Schlüssel für die erste Spalte der [Component-Tabelle.](component-table.md) Diese Spalte verweist auf die Komponente, die die Installation der Umgebungswerte steuert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Damit das Installationsprogramm Umgebungsvariablen festlegen kann, müssen die [Aktion WriteEnvironmentStrings](writeenvironmentstrings-action.md) und [die Aktion RemoveEnvironmentStrings](removeenvironmentstrings-action.md) in der Tabelle [InstallExecuteSequence](installexecutesequence-table.md)aufgeführt werden.

Beachten Sie, dass sich Umgebungsvariablen für die derzeit ausgeführte Installation nicht ändern, wenn entweder die [Aktion WriteEnvironmentStrings](writeenvironmentstrings-action.md) oder [die Aktion RemoveEnvironmentStrings](removeenvironmentstrings-action.md) ausgeführt werden. Am Windows 2000 werden diese Informationen in der Registrierung gespeichert, und eine Meldung benachrichtigt das System über Änderungen, wenn die Installation abgeschlossen ist. Ein neuer Prozess oder ein anderer Prozess, der nach diesen Nachrichten sucht, verwendet die neuen Umgebungsvariablen.

Wenn Sie die Umgebungsvariable path mit der Umgebungstabelle ändern, versuchen Sie nicht, den gesamten neuen Pfad explizit in das Feld Wert einzugeben. Erweitern Sie stattdessen den vorhandenen Pfad, indem Sie einen Wert und ein Trennzeichen voransetzen oder anfügen (;) zu \[ ~ \] . Wenn nicht im Feld Wert vorhanden ist, werden \[ ~ \] die vorhandenen Pfadinformationen verloren, und die Installation der .msi-Datei kann das Starten des Computers verhindern. Die Pfadvariable wird häufig mithilfe der Folgenden festgelegt: \[ ~ \] ; Wert.

Beim Ausführen computerbasierter Installationen von einem Terminalserver schreibt das Installationsprogramm Benutzerspezifische Umgebungsvariablen in die **HKU \\ . \\Standardumgebung**. Da terminal services diesen Abschnitt der Registrierung nicht repliziert, werden bei der Installation die Benutzerumgebungsvariablen nicht festgelegt. Ein Paket, das für computerspezifische Installationen verwendet wird, sollte Umgebungsvariablen in die Umgebung des Computers schreiben, indem \* es in die Spalte Name eingeschlossen wird. Wenn das Paket pro Benutzer oder pro Computer installiert werden kann, erstellen Sie zwei Komponenten: (1) eine Pro-Benutzer-Komponente mit den Umgebungstabelleneinträgen, die für Benutzereinstellungen erstellt wurden, und (2) eine Komponente pro Computer mit der Umgebungstabelle, die für Computereinstellungen erstellt wurde. Bedingung für die Installation dieser Komponente mithilfe der [**Privileged-Eigenschaft.**](privileged.md)

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE65](ice65.md)  
[ICE69](ice69.md)  
[ICE80](ice80.md)  
</dl>

 

 




