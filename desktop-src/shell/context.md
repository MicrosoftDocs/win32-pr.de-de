---
description: Wenn Sie mit der rechten Maustaste auf ein Objekt klicken, wird normalerweise ein Kontextmenü angezeigt. Dieses Menü enthält eine Liste mit Befehlen, die der Benutzer auswählen kann, um verschiedene Aktionen für das Objekt auszuführen. Dieser Abschnitt ist eine Einführung in Kontextmenüs für Dateisystem Objekte.
ms.assetid: d951d1e8-0f88-49c4-8373-e6db0e18cd72
title: Erweitern von Kontextmenüs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895550ff050d559b3523676ddaa2a58099398a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566351"
---
# <a name="extending-shortcut-menus"></a>Erweitern von Kontextmenüs

Wenn Sie mit der rechten Maustaste auf ein Objekt klicken, wird normalerweise ein Kontext *Menü* angezeigt. Dieses Menü enthält eine Liste mit Befehlen, die der Benutzer auswählen kann, um verschiedene Aktionen für das Objekt auszuführen. Dieser Abschnitt ist eine Einführung in Kontextmenüs für Dateisystem Objekte.

-   [Kontextmenüs für Datei System Objekte](#shortcut-menus-for-file-system-objects)
-   [Kontextmenü Verben](#shortcut-menu-verbs)
    -   [Kanonische Verben](#canonical-verbs)
    -   [Erweiterte Verben](#extended-verbs)
-   [Erweitern des Kontextmenüs für einen Dateityp](#extending-the-shortcut-menu-for-a-file-type)
-   [Erweitern des Kontextmenüs für vordefinierte Shellobjekte](#extending-the-shortcut-menu-for-predefined-shell-objects)
-   [Registrieren einer Anwendung zum Verarbeiten beliebiger Dateitypen](#registering-an-application-to-handle-arbitrary-file-types)
-   [Erweitern des neuen Untermenüs](#extending-the-new-submenu)

Weitere Informationen finden Sie hier:

-   [Definieren erweiterter Verben](how-to-define-extended-verbs.md)
-   [Zuordnen von Verben zu DDE-Befehlen](how-to-associate-verbs-with-dde-commands.md)

## <a name="shortcut-menus-for-file-system-objects"></a>Kontextmenüs für Datei System Objekte

Wenn ein Benutzer mit der rechten Maustaste auf ein Objekt (z. b. eine Datei) klickt, das in Windows-Explorer oder auf dem Desktop angezeigt wird, wird ein Kontextmenü mit einer Liste von Befehlen angezeigt. Der Benutzer kann dann eine Aktion für die Datei durchführen, z. b. Öffnen oder löschen, indem er den entsprechenden Befehl auswählt.

Da für die Dateiverwaltung häufig Kontextmenüs verwendet werden, stellt die Shell eine Reihe von Standard Befehlen, z. b. Ausschneiden und kopieren, bereit, die im Kontextmenü für eine beliebige Datei angezeigt werden. Obwohl Open with ein Standardbefehl ist, wird es für einige Standard Dateitypen, z. b. wav, nicht angezeigt. Die folgende Abbildung des Beispiels Verzeichnis "eigene Dateien", das auch als Beispiel für das [Anpassen von Symbolen](icon.md)verwendet wurde, zeigt ein Standardkontext Menü, das angezeigt wird, wenn Sie mit der rechten Maustaste auf "MyDocs4.xyz" klicken.

![Screenshot des Standardkontext Menüs für Dateisystem Objekte](images/context1.jpg)

Der Grund dafür, dass MyDocs4.xyz ein Standardkontext Menü anzeigt, ist, dass es kein Member eines registrierten [Dateityps](fa-file-types.md)ist. Auf der anderen Seite ist ". txt" ein registrierter Dateityp. Wenn Sie mit der rechten Maustaste auf eine der txt-Dateien klicken, wird stattdessen ein Kontextmenü mit zwei zusätzlichen Befehlen im oberen Abschnitt angezeigt: **Öffnen** und **Drucken**.

![Screenshot des angepassten Kontextmenüs für Dateisystem Objekte](images/context2.jpg)

Sobald ein Dateityp registriert ist, können Sie das Kontextmenü mit zusätzlichen Befehlen erweitern. Sie werden oberhalb der Standard Befehle angezeigt, wenn mit der rechten Maustaste auf eine Datei dieses Typs geklickt wird. Obwohl die meisten Befehle, die auf diese Weise hinzugefügt werden, häufig vorkommen, wie z. b. **Drucken** oder **Öffnen**, können Sie jeden beliebigen Befehl hinzufügen, den ein Benutzer hilfreich finden kann.

Um das Kontextmenü für einen Dateityp zu erweitern, müssen Sie lediglich einen Registrierungs Eintrag für jeden Befehl erstellen. Ein anspruchsvolleres Verfahren besteht darin, einen Kontext *Menü Handler* zu implementieren, mit dem Sie das Kontextmenü für einen Dateityp Datei-für-Datei-Basis erweitern können. Weitere Informationen finden Sie unter [Erstellen von Kontextmenü Handlern](context-menu-handlers.md).

## <a name="shortcut-menu-verbs"></a>Kontextmenü Verben

Jeder Befehl im Kontextmenü wird durch sein *Verb* in der Registrierung identifiziert. Diese Verben sind identisch mit denen, die von [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) verwendet werden, wenn Anwendungen Programm gesteuert gestartet werden. Weitere Informationen zur Verwendung von **ShellExecuteEx** finden Sie in der Diskussion unter [Starten von Anwendungen](launch.md).

Ein Verb ist eine einfache Text Zeichenfolge, die von der Shell verwendet wird, um den zugehörigen Befehl zu identifizieren. Jedes Verb entspricht der *Befehls Zeichenfolge* , die verwendet wird, um den Befehl in einem Konsolenfenster oder einer Batchdatei (. bat) zu starten. Beispielsweise wird im **geöffneten** Verb normalerweise ein Programm zum Öffnen einer Datei gestartet. Die Befehls Zeichenfolge sieht in der Regel etwa wie folgt aus:

``` syntax
"My Program.exe" "%1"
```

"%1" ist der Standard Platzhalter für einen Befehlszeilenparameter, der mit dem Dateinamen angegeben wird. Beispielsweise kann eine bestimmte Seite angegeben werden, die in einer Ansicht im Registerkarten Format angezeigt werden soll.

> [!Note]  
> Wenn ein beliebiges Element der Befehls Zeichenfolge Leerzeichen enthält, muss es in Anführungszeichen eingeschlossen werden. Wenn das Element ein Leerzeichen enthält, wird es andernfalls nicht ordnungsgemäß analysiert. Beispielsweise wird die Anwendung mit "My Program.exe" ordnungsgemäß gestartet. Wenn Sie meine Program.exe verwenden, versucht das System, "My" mit "Program.exe" als erstes Befehlszeilenargument zu starten. Sie sollten immer Anführungszeichen mit Argumenten wie "%1" verwenden, die von der Shell auf Zeichen folgen erweitert werden, da Sie nicht sicher sein können, dass die Zeichenfolge kein Leerzeichen enthält.

 

Verben können auch eine *Anzeige Zeichenfolge* zugeordnet werden, die im Kontextmenü anstelle der Verb Zeichenfolge selbst angezeigt wird. Beispielsweise ist die Anzeige Zeichenfolge für **openas** mit geöffnet. Wie normale Menü Zeichenfolgen, einschließlich eines kaufmännischen und-Zeichens (&) in der Anzeige Zeichenfolge, wird die Tastaturauswahl des Befehls ermöglicht.

### <a name="canonical-verbs"></a>Kanonische Verben

Im Allgemeinen sind Anwendungen für die Bereitstellung lokalisierter Anzeige Zeichenfolgen für die Verben zuständig, die Sie definieren. Um jedoch eine gewisse Sprachunabhängigkeit zu gewährleisten, definiert das System einen Standardsatz häufig verwendeter Verben, die als *kanonische Verben* bezeichnet werden. Ein kanonisches Verb kann in jeder Sprache verwendet werden, und das System generiert automatisch eine ordnungsgemäß lokalisierte Anzeige Zeichenfolge. Die Anzeige Zeichenfolge des **geöffneten** Verbs wird beispielsweise auf einem englischen System geöffnet und kann auf einem deutschen System geöffnet werden.

Die kanonischen Verben umfassen Folgendes:



| Wert      | BESCHREIBUNG                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| open       | Öffnet die Datei oder den Ordner.                                                                   |
| OpenNew    | Öffnet die Datei oder den Ordner in einem neuen Fenster.                                                   |
| print      | Druckt die Datei.                                                                            |
| explore    | Öffnet den Windows-Explorer mit ausgewähltem Ordner.                                            |
| Suchen       | Öffnet das Dialogfeld **Windows-Suche** , in dem der Ordner als Standard Such Speicherort festgelegt ist. |
| openas     | Öffnet das Dialogfeld **Öffnen mit** .                                                         |
| properties | Öffnet das Eigenschaften Blatt des-Objekts.                                                          |



 

Das Printto-Verb ist auch kanonisch, wird aber nie angezeigt. Dadurch kann der Benutzer eine Datei drucken, indem er Sie auf ein Drucker Objekt zieht.

### <a name="extended-verbs"></a>Erweiterte Verben

Wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt, enthält das Kontextmenü alle normalen Verben. Es können jedoch Befehle vorhanden sein, die Sie unterstützen möchten, aber nicht in jedem Kontextmenü angezeigt werden. Beispielsweise können Sie über Befehle verfügen, die nicht häufig verwendet werden oder für erfahrene Benutzer gedacht sind. Aus diesem Grund können Sie auch ein oder mehrere *Erweiterte Verben* definieren. Diese Verben sind ebenfalls Zeichen folgen und ähneln normalen Verben. Sie unterscheiden sich von normalen Verben durch die Art und Weise, wie Sie registriert werden. Um Zugriff auf die mit erweiterten Verben verknüpften Befehle zu erhalten, muss der Benutzer mit der rechten Maustaste auf ein Objekt klicken, während er die UMSCHALTTASTE drückt. Die erweiterten Verben werden dann zusammen mit den normalen Verben angezeigt.

## <a name="extending-the-shortcut-menu-for-a-file-type"></a>Erweitern des Kontextmenüs für einen Dateityp

Die einfachste Möglichkeit, das Kontextmenü für einen Dateityp zu erweitern, ist die Registrierung. Fügen Sie hierzu unter dem Schlüssel für die ProgID der Anwendung, die dem [Dateityp](fa-file-types.md)zugeordnet ist, einen **shellunterschlüssel** hinzu. Optional können Sie ein Standard- *Verb* für den Dateityp definieren, indem Sie es als Standardwert für den **shellunterschlüssel** festlegen.

Das Standardverb wird zuerst im Kontextmenü angezeigt. Der Zweck besteht darin, die Shell mit einem Verb zu versehen, das Sie verwenden kann, wenn [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) aufgerufen wird, aber kein Verb angegeben wird. Die Shell wählt nicht notwendigerweise das Standard Verb aus, wenn **ShellExecuteEx** auf diese Weise verwendet wird. Für Shell- [Versionen 5,0](versions.md) und höher, die auf Systemen unter Windows 2000 und höher gefunden werden, verwendet die Shell das erste verfügbare Verb aus der folgenden Liste. Wenn keine verfügbar sind, schlägt der Vorgang fehl.

-   Das geöffnete Verb
-   Das Standardverb
-   Das erste Verb in der Registrierung
-   Das openWith-Verb

Lassen Sie für Shell-Versionen vor [Version 5,0](versions.md)das dritte Element aus.

Erstellen Sie unter dem **shellunterschlüssel** einen Unterschlüssel für jedes Verb, das Sie hinzufügen möchten. Für jeden dieser Unterschlüssel wird ein **reg \_ SZ** -Wert auf die Anzeige Zeichenfolge des Verbs festgelegt. Sie können die Anzeige Zeichenfolge für kanonische Verben weglassen, da das System automatisch eine ordnungsgemäß lokalisierte Zeichenfolge anzeigt. Wenn Sie die Anzeige Zeichenfolge für nicht kanonische Verben weglassen, wird die Verb Zeichenfolge angezeigt. Erstellen Sie für jeden Verb Unterschlüssel einen **Befehls** Unterschlüssel, bei dem der Standardwert auf die Befehls Zeichenfolge festgelegt ist.

Die folgende Abbildung zeigt ein Kontextmenü für den MYP-Dateityp, der in [Dateitypen](fa-file-types.md) und [Anpassen von Symbolen](icon.md)verwendet wird. Sie verfügt jetzt über das Kontextmenü mit den Verben "Open", "doit", "Print" und "Printto" und "doit" als Standard Verb Das Kontextmenü sieht wie folgt aus.

![Screenshot des angepassten Kontextmenüs](images/context3.jpg)

Die Registrierungseinträge, die verwendet werden, um das in der obigen Abbildung gezeigte Kontextmenü zu erweitern, sind:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

Obwohl der Befehl **Öffnen mit** über dem ersten Trennzeichen liegt, wird er automatisch vom System erstellt und erfordert keinen Registrierungs Eintrag. Das System erstellt automatisch anzeigen Amen für die kanonischen Verben Open und Print. Da es sich bei doit nicht um ein kanonisches Verb handelt, wird ihm ein Anzeige Name ("&do this") zugewiesen, der durch Drücken der D-Taste ausgewählt werden kann. Das Printto-Verb wird nicht im Kontextmenü angezeigt, aber das Einschließen von Dateien ermöglicht dem Benutzer das Drucken von Dateien, indem Sie Sie auf einem Druckersymbol ablegen. In diesem Beispiel stellt "%1" den Dateinamen und "%2" für den Drucker Namen dar.

Verben können durch Richtlinien Einstellungen unterdrückt werden, indem Sie dem Schlüssel des Verbs einen SuppressionPolicy-Wert hinzufügen. Legen Sie den Wert von SuppressionPolicy auf die Richtlinien-ID fest. Wenn die Richtlinie aktiviert ist, werden das Verb und der zugehörige Kontextmenü Eintrag unterdrückt. Mögliche Richtlinien-ID-Werte finden Sie unter der [**Einschränkungs**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) Enumeration.

## <a name="extending-the-shortcut-menu-for-predefined-shell-objects"></a>Erweitern des Kontextmenüs für vordefinierte Shellobjekte

Viele vordefinierte Shellobjekte verfügen über Kontextmenüs, die erweitert werden können. Registrieren Sie den Befehl auf die gleiche Weise, wie Sie typische Dateitypen registrieren, aber verwenden Sie den Namen des vordefinierten Objekts als Dateityp Namen.

Eine Liste der vordefinierten Objekte finden Sie im Abschnitt " *vordefinierte Shellobjekte* " unter [Erstellen von Shellerweiterungs Handlern](handlers.md). Die vordefinierten Shellobjekte, deren Kontextmenüs durch das Hinzufügen von Verben in der Registrierung erweitert werden können, werden in der Tabelle mit dem Wort "Verb" markiert.

## <a name="registering-an-application-to-handle-arbitrary-file-types"></a>Registrieren einer Anwendung zum Verarbeiten beliebiger Dateitypen

In den vorherigen Abschnitten dieses Dokuments wurde erläutert, wie Kontextmenü Elemente für einen bestimmten Dateityp definiert werden. Unter anderem können Sie das Kontextmenü definieren, um anzugeben, wie die zugehörige Anwendung einen Member des Dateityps öffnet. Wie in [Dateitypen](fa-file-types.md)erläutert, können Anwendungen jedoch auch eine separate Standardprozedur registrieren, die verwendet wird, wenn ein Benutzer versucht, die Anwendung zu verwenden, um einen Dateityp zu öffnen, der nicht der Anwendung zugeordnet ist. Dieses Thema wird hier erläutert, da Sie das Standardverfahren auf die gleiche Weise registrieren wie beim Registrieren von Kontextmenü Elementen.

Die Standardprozedur dient zwei grundlegenden Zwecken. Eine besteht darin, anzugeben, wie die Anwendung aufgerufen werden soll, um einen beliebigen Dateityp zu öffnen. Beispielsweise können Sie ein befehlszeilenflag verwenden, um anzugeben, dass ein Unbekannter Dateityp geöffnet wird. Der andere Zweck besteht darin, die verschiedenen Merkmale eines Dateityps zu definieren, z. b. die Kontextmenü Elemente und das Symbol. Wenn ein Benutzer die Anwendung einem zusätzlichen Dateityp zuordnet, hat dieser Typ diese Merkmale. Wenn der zusätzliche Dateityp zuvor mit einer anderen Anwendung verknüpft war, werden die Original Eigenschaften durch diese Merkmale ersetzt.

Um die Standardprozedur zu registrieren, platzieren Sie die gleichen Registrierungsschlüssel, die Sie für die ProgID Ihrer Anwendung erstellt haben, unter dem Unterschlüssel der Anwendung von **HKEY \_ Classes \_ root** \\ **Applications**. Sie können auch einen friendlyappname-Wert einschließen, um dem System einen anzeigen Amen für die Anwendung bereitzustellen. Der Anzeige Name der Anwendung kann auch aus der ausführbaren Datei extrahiert werden, jedoch nur, wenn der friendlyappname-Wert nicht vorhanden ist. Das folgende Registrierungs Fragment zeigt eine Beispiel-Standardprozedur für MyProgram.exe, die einen anzeigen Amen und mehrere Kontextmenü Elemente definiert. Die Befehls Zeichenfolgen enthalten das Flag/a, um die Anwendung darüber zu benachrichtigen, dass ein beliebiger Dateityp geöffnet wird. Wenn Sie einen **DefaultIcon** -Unterschlüssel einschließen, sollten Sie ein generisches Symbol verwenden.

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         FriendlyAppName = Friendly Name
         shell
            open
               command
                  (Default) = C:\MyDir\MyProgram.exe /a "%1"
            print
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
            printto
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2" %3 %4
```

## <a name="extending-the-new-submenu"></a>Erweitern des neuen Untermenüs

Wenn ein Benutzer das Menü **Datei** in Windows-Explorer öffnet, ist der erste Befehl **neu**. Wenn Sie diesen Befehl auswählen, wird ein Untermenü angezeigt. Standardmäßig enthält er zwei **Befehle,** **Ordner** und Verknüpfungen, mit denen Benutzer Unterordner und Verknüpfungen erstellen können. Dieses Untermenü kann so erweitert werden, dass es Datei Erstellungs Befehle für einen beliebigen Dateityp einschließt.

Um dem **neuen** Untermenü einen Befehl zum Erstellen von Dateien hinzuzufügen, muss den Dateien Ihrer Anwendung ein [Dateityp](fa-file-types.md) zugeordnet sein. Fügen Sie einen **ShellNew** -Unterschlüssel unter dem Schlüssel für die Dateinamenerweiterung ein. Wenn der **neue** Befehl im Menü **Datei** ausgewählt ist, wird er von der Shell dem **neuen** Untermenü hinzugefügt. Die Anzeige Zeichenfolge des Befehls ist die beschreibende Zeichenfolge, die der ProgID des Programms zugewiesen wird.

Weisen Sie dem **ShellNew** -Unterschlüssel einen oder mehrere Datenwerte zu, um die Datei Erstellungs Methode anzugeben. Die folgenden Werte sind verfügbar.



| Wert    | BESCHREIBUNG                                                                                                                                                   |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Befehl  | Führt eine Anwendung aus. Dies ist ein **reg \_ SZ** -Wert, der den Pfad der Anwendung angibt, die ausgeführt werden soll. Beispielsweise können Sie festlegen, dass ein Assistent gestartet wird. |
| Daten     | Erstellt eine Datei mit den angegebenen Daten. Daten sind ein **reg- \_ Binärwert** mit den Daten der Datei. Die Daten werden ignoriert, wenn entweder die nulldatei oder der Dateiname angegeben wird.  |
| FileName | Erstellt eine Datei, die eine Kopie einer angegebenen Datei ist. FileName ist ein **reg \_ SZ** -Wert, der auf den voll qualifizierten Pfad der zu kopierenden Datei festgelegt wird.                 |
| Nulldatei | Erstellt eine leere Datei. NullFile wurde kein Wert zugewiesen. Wenn NullFile angegeben ist, werden die Daten-und Dateinamen Werte ignoriert.                                  |



 

Die folgende Abbildung zeigt das **neue** Untermenü für den MYP-Dateityp, der als Beispiel in [Dateitypen](fa-file-types.md) und [Anpassen von Symbolen](icon.md)verwendet wird. Sie verfügt jetzt über den Befehl **myprogram Application**. Wenn ein Benutzer im Untermenü **neu** die Option **myprogram-Anwendung** auswählt, erstellt die Shell eine Datei mit dem Namen "New myprogram Application. MYP" und übergibt sie an MyProgram.exe.

![Screenshot des benutzerdefinierten Menüs "neu"](images/context5.png)

Der Registrierungs Eintrag lautet nun wie folgt:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
            NullFile
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 



