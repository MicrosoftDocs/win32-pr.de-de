---
description: Wenn Sie mit der rechten Maustaste auf ein Objekt klicken, wird normalerweise ein Kontextmenü angezeigt. Dieses Menü enthält eine Liste der Befehle, die der Benutzer auswählen kann, um verschiedene Aktionen für das Objekt auszuführen. Dieser Abschnitt enthält eine Einführung in Kontextmenüs für Dateisystemobjekte.
ms.assetid: d951d1e8-0f88-49c4-8373-e6db0e18cd72
title: Erweitern von Kontextmenüs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d046805ebc787f5cad2bfaa40538c51b826c3f0541f3ec1afad508202a4a25fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460647"
---
# <a name="extending-shortcut-menus"></a>Erweitern von Kontextmenüs

Wenn Sie mit der rechten Maustaste auf ein Objekt klicken, wird normalerweise ein *Kontextmenü* angezeigt. Dieses Menü enthält eine Liste der Befehle, die der Benutzer auswählen kann, um verschiedene Aktionen für das Objekt auszuführen. Dieser Abschnitt enthält eine Einführung in Kontextmenüs für Dateisystemobjekte.

-   [Kontextmenüs für Dateisystemobjekte](#shortcut-menus-for-file-system-objects)
-   [Verknüpfungsmenüverben](#shortcut-menu-verbs)
    -   [Kanonische Verben](#canonical-verbs)
    -   [Erweiterte Verben](#extended-verbs)
-   [Erweitern des Kontextmenüs für einen Dateityp](#extending-the-shortcut-menu-for-a-file-type)
-   [Erweitern des Kontextmenüs für vordefinierte Shellobjekte](#extending-the-shortcut-menu-for-predefined-shell-objects)
-   [Registrieren einer Anwendung für die Verarbeitung beliebiger Dateitypen](#registering-an-application-to-handle-arbitrary-file-types)
-   [Erweitern des neuen Untermenüs](#extending-the-new-submenu)

Weitere Informationen finden Sie hier:

-   [Definieren von erweiterten Verben](how-to-define-extended-verbs.md)
-   [Zuordnen von Verben zu DDE-Befehlen](how-to-associate-verbs-with-dde-commands.md)

## <a name="shortcut-menus-for-file-system-objects"></a>Kontextmenüs für Dateisystemobjekte

Wenn ein Benutzer mit der rechten Maustaste auf ein Objekt klickt, z. B. auf eine Datei, die im Windows Explorer oder auf dem Desktop angezeigt wird, wird ein Kontextmenü mit einer Liste von Befehlen angezeigt. Der Benutzer kann dann eine Aktion für die Datei ausführen, z. B. öffnen oder löschen, indem er den entsprechenden Befehl auswählt.

Da Kontextmenüs häufig für die Dateiverwaltung verwendet werden, stellt die Shell eine Reihe von Standardbefehlen wie Ausschneiden und Kopieren bereit, die im Kontextmenü für jede Datei angezeigt werden. Beachten Sie, dass Open With zwar ein Standardbefehl ist, aber für einige Standarddateitypen, z. B. WAV, nicht angezeigt wird. Die folgende Abbildung des Beispielverzeichnisses Eigene Dokumente, das auch als Beispiel in Anpassen von [Symbolen](icon.md)verwendet wurde, zeigt ein Standardverknüpfungsmenü, das durch Klicken mit der rechten Maustaste auf MyDocs4.xyz angezeigt wurde.

![Screenshot des Standardverknüpfungsmenüs für Dateisystemobjekte](images/context1.jpg)

Der Grund dafür, dass MyDocs4.xyz ein Standardverknüpfungsmenü anzeigt, ist, dass es kein Member eines registrierten [Dateityps](fa-file-types.md)ist. Andererseits ist .txt ein registrierter Dateityp. Wenn Sie mit der rechten Maustaste auf eine der .txt Dateien klicken, wird stattdessen ein Kontextmenü mit zwei zusätzlichen Befehlen im oberen Abschnitt angezeigt: **Öffnen** und **Drucken.**

![Screenshot des angepassten Kontextmenüs für Dateisystemobjekte](images/context2.jpg)

Nachdem ein Dateityp registriert wurde, können Sie das Kontextmenü mit zusätzlichen Befehlen erweitern. Sie werden über den Standardbefehlen angezeigt, wenn mit der rechten Maustaste auf eine Datei dieses Typs geklickt wird. Obwohl die meisten der auf diese Weise hinzugefügten Befehle häufig verwendet werden, z. B. **Drucken** oder **Öffnen,** können Sie beliebige Befehle hinzufügen, die ein Benutzer möglicherweise hilfreich finden kann.

Zum Erweitern des Kontextmenüs für einen Dateityp ist nur das Erstellen eines Registrierungseintrags für jeden Befehl erforderlich. Ein komplexerer Ansatz besteht darin, einen *Kontextmenühandler* zu implementieren, mit dem Sie das Kontextmenü für einen Dateityp dateiweise erweitern können. Weitere Informationen finden Sie unter [Erstellen von Kontextmenühandlern.](context-menu-handlers.md)

## <a name="shortcut-menu-verbs"></a>Verknüpfungsmenüverben

Jeder Befehl im Kontextmenü wird in der Registrierung durch das *Verb* identifiziert. Diese Verben sind identisch mit denen, die von [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) beim programmgesteuerten Starten von Anwendungen verwendet werden. Weitere Informationen zur Verwendung von **ShellExecuteEx** finden Sie in der Diskussion unter [Starten von Anwendungen.](launch.md)

Ein Verb ist eine einfache Textzeichenfolge, die von der Shell verwendet wird, um den zugeordneten Befehl zu identifizieren. Jedes Verb entspricht der *Befehlszeichenfolge,* die zum Starten des Befehls in einem Konsolenfenster oder einer Batchdatei (.bat) verwendet wird. Beispielsweise startet das **geöffnete** Verb normalerweise ein Programm, um eine Datei zu öffnen. Die Befehlszeichenfolge sieht in der Regel in etwa wie folgt aus:

``` syntax
"My Program.exe" "%1"
```

"%1" ist der Standardplatzhalter für einen Befehlszeilenparameter, der mit dem Dateinamen bereitgestellt wird. Beispielsweise kann eine bestimmte Seite angegeben werden, die in einer Ansicht im Registerkartenbett angezeigt werden soll.

> [!Note]  
> Wenn ein Element der Befehlszeichenfolge Leerzeichen enthält oder enthalten kann, muss es in Anführungszeichen eingeschlossen werden. Wenn das Element ein Leerzeichen enthält, wird es andernfalls nicht ordnungsgemäß analysiert. Beispielsweise startet "My Program.exe" die Anwendung ordnungsgemäß. Wenn Sie My Program.exe verwenden, versucht das System, "My" mit "Program.exe" als erstes Befehlszeilenargument zu starten. Sie sollten immer Anführungszeichen mit Argumenten wie "%1" verwenden, die von der Shell auf Zeichenfolgen erweitert werden, da Sie nicht sicher sein können, dass die Zeichenfolge kein Leerzeichen enthält.

 

Verben kann auch eine *Anzeigezeichenfolge* zugeordnet sein, die im Kontextmenü anstelle der Verbzeichenfolge selbst angezeigt wird. Die Anzeigezeichenfolge für **openas** lautet z. B. Open With. Wie normale Menüzeichenfolgen ermöglicht das Einschließen eines ampersand (&) in der Anzeigezeichenfolge die Tastaturauswahl des Befehls.

### <a name="canonical-verbs"></a>Kanonische Verben

Im Allgemeinen sind Anwendungen für die Bereitstellung lokalisierter Anzeigezeichenfolgen für die von ihnen definierten Verben verantwortlich. Um jedoch ein gewisses Maß an Sprachunabhängigkeit zu gewährleisten, definiert das System einen Standardsatz häufig verwendeter Verben, die als *kanonische Verben* bezeichnet werden. Ein kanonisches Verb kann mit jeder Sprache verwendet werden, und das System generiert automatisch eine ordnungsgemäß lokalisierte Anzeigezeichenfolge. Beispielsweise wird die Anzeigezeichenfolge des **geöffneten** Verbs auf Öffnen auf einem englischen System und auf Öffnen auf einem deutschen System festgelegt.

Zu den kanonischen Verben gehören:



| Wert      | Beschreibung                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| öffnen       | Öffnet die Datei oder den Ordner.                                                                   |
| opennew    | Öffnet die Datei oder den Ordner in einem neuen Fenster.                                                   |
| print      | Gibt die Datei aus.                                                                            |
| explore    | Öffnet Windows Explorer mit dem ausgewählten Ordner.                                            |
| Suchen       | Öffnet das Dialogfeld **Windows Suchen,** in dem der Ordner als Standardspeicherort für die Suche festgelegt ist. |
| openas     | Öffnet das Dialogfeld **Öffnen mit** .                                                         |
| properties | Öffnet das Eigenschaftenblatt des Objekts.                                                          |



 

Das printto-Verb ist ebenfalls kanonisch, wird aber nie angezeigt. Der Benutzer kann eine Datei drucken, indem er sie auf ein Druckerobjekt zieht.

### <a name="extended-verbs"></a>Erweiterte Verben

Wenn der Benutzer mit der rechten Maustaste auf ein Objekt klickt, enthält das Kontextmenü alle normalen Verben. Es können jedoch Befehle vorhanden sein, die Sie unterstützen möchten, aber nicht in jedem Kontextmenü angezeigt wurden. Beispielsweise können Sie Befehle verwenden, die nicht häufig verwendet werden oder für erfahrene Benutzer vorgesehen sind. Aus diesem Grund können Sie auch ein oder mehrere *erweiterte Verben* definieren. Diese Verben sind auch Zeichenfolgen und ähneln normalen Verben. Sie unterscheiden sich durch ihre Registrierung von normalen Verben. Um Zugriff auf die Befehle zu erhalten, die erweiterten Verben zugeordnet sind, muss der Benutzer mit der rechten Maustaste auf ein Objekt klicken, während er die UMSCHALTTASTE drückt. Die erweiterten Verben werden dann zusammen mit den normalen Verben angezeigt.

## <a name="extending-the-shortcut-menu-for-a-file-type"></a>Erweitern des Kontextmenüs für einen Dateityp

Die einfachste Möglichkeit, das Kontextmenü für einen Dateityp zu erweitern, ist die Registrierung. Fügen Sie hierzu  einen Shell-Unterschlüssel unterhalb des Schlüssels für die ProgID der Anwendung hinzu, die dem [Dateityp](fa-file-types.md)zugeordnet ist. Optional können Sie ein *Standardverb* für den Dateityp definieren, indem Sie es als Standardwert des Shell-Unterschlüssels festlegen. 

Das Standardverb wird zuerst im Kontextmenü angezeigt. Der Zweck besteht darin, der Shell ein Verb bereitzustellen, das sie verwenden kann, wenn [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) aufgerufen wird, aber kein Verb angegeben wird. Die Shell wählt nicht unbedingt das Standardverb aus, wenn **ShellExecuteEx** auf diese Weise verwendet wird. Für die [Shell-Versionen 5.0](versions.md) und höher, die auf Windows 2000- und höher-Systemen gefunden werden, verwendet die Shell das erste verfügbare Verb aus der folgenden Liste. Wenn keine verfügbar sind, schlägt der Vorgang fehl.

-   Das geöffnete Verb
-   Das Standardverb
-   Das erste Verb in der Registrierung
-   Das openwith-Verb

Lassen Sie für Shell-Versionen vor [Version 5.0](versions.md)das dritte Element aus.

Erstellen  Sie unterhalb des Shell-Unterschlüssels einen Unterschlüssel für jedes Verb, das Sie hinzufügen möchten. Für jeden dieser Unterschlüssel wird ein **REG \_ SZ-Wert** auf die Anzeigezeichenfolge des Verbs festgelegt. Sie können die Anzeigezeichenfolge für kanonische Verben weglassen, da das System automatisch eine ordnungsgemäß lokalisierte Zeichenfolge anzeigt. Wenn Sie die Anzeigezeichenfolge für nicht kanonische Verben weglassen, wird die Verbzeichenfolge angezeigt. Erstellen Sie für jeden  Verbunterschlüssel einen Befehlsunterschlüssel, wobei der Standardwert auf die Befehlszeichenfolge festgelegt ist.

Die folgende Abbildung zeigt ein Kontextmenü für den .myp-Dateityp, der in [Dateitypen](fa-file-types.md) und [Anpassen von Symbolen](icon.md)verwendet wird. Sie verfügt nun über verbs open, doit, print und printto im Kontextmenü, wobei doit das Standardverb ist. Das Kontextmenü sieht wie folgt aus.

![Screenshot des angepassten Kontextmenüs](images/context3.jpg)

Die Registrierungseinträge, die zum Erweitern des Kontextmenüs in der vorherigen Abbildung verwendet werden, lauten wie folgt:

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

Obwohl sich der Befehl **Open With** oberhalb des ersten Trennzeichens befindet, wird er automatisch vom System erstellt und erfordert keinen Registrierungseintrag. Das System erstellt automatisch Anzeigenamen für die kanonischen Verben, die geöffnet und gedruckt werden. Da doit kein kanonisches Verb ist, wird ihm der Anzeigename "&Do It" zugewiesen, der durch Drücken der D-Taste ausgewählt werden kann. Das Printto-Verb wird nicht im Kontextmenü angezeigt, ermöglicht dem Benutzer jedoch das Drucken von Dateien, indem er sie auf einem Druckersymbol ablegen kann. In diesem Beispiel stellt %1 den Dateinamen und %2 den Druckernamen dar.

Verben können über Richtlinieneinstellungen unterdrückt werden, indem dem Schlüssel des Verbs ein SuppressionPolicy-Wert hinzugefügt wird. Legen Sie den Wert von SuppressionPolicy auf die Richtlinien-ID fest. Wenn die Richtlinie aktiviert ist, werden das Verb und der zugehörige Kontextmenüeintrag unterdrückt. Mögliche Richtlinien-ID-Werte finden Sie unter [**RESTRICTIONS-Enumeration.**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions)

## <a name="extending-the-shortcut-menu-for-predefined-shell-objects"></a>Erweitern des Kontextmenüs für vordefinierte Shellobjekte

Viele vordefinierte Shell-Objekte verfügen über Kontextmenüs, die erweitert werden können. Registrieren Sie den Befehl auf die gleiche Weise wie typische Dateitypen, verwenden Sie jedoch den Namen des vordefinierten Objekts als Dateitypnamen.

Eine Liste vordefinierter Objekte finden Sie im Abschnitt *Vordefinierte Shellobjekte* unter [Erstellen von Shellerweiterungshandlern.](handlers.md) Vordefinierte Shell-Objekte, deren Kontextmenüs durch Hinzufügen von Verben in der Registrierung erweitert werden können, werden in der Tabelle mit dem Wort "Verb" markiert.

## <a name="registering-an-application-to-handle-arbitrary-file-types"></a>Registrieren einer Anwendung für die Verarbeitung beliebiger Dateitypen

In den vorherigen Abschnitten dieses Dokuments wurde erläutert, wie Kontextmenüelemente für einen bestimmten Dateityp definiert werden. Durch das Definieren des Kontextmenüs können Sie unter anderem angeben, wie die zugeordnete Anwendung einen Member des Dateityps öffnet. Wie unter [Dateitypen](fa-file-types.md)erläutert, können Anwendungen jedoch auch eine separate Standardprozedur registrieren, die verwendet werden soll, wenn ein Benutzer versucht, ihre Anwendung zum Öffnen eines Dateityps zu verwenden, den Sie der Anwendung nicht zugeordnet haben. Dieses Thema wird hier erläutert, da Sie die Standardprozedur auf ähnliche Weise registrieren wie Kontextmenüelemente.

Die Standardprozedur dient zwei grundlegenden Zwecken. Eine möglichkeit besteht darin, anzugeben, wie Ihre Anwendung aufgerufen werden soll, um einen beliebigen Dateityp zu öffnen. Sie können z. B. ein Befehlszeilenflag verwenden, um anzugeben, dass ein unbekannter Dateityp geöffnet wird. Der andere Zweck besteht darin, die verschiedenen Merkmale eines Dateityps zu definieren, z. B. die Kontextmenüelemente und das Symbol. Wenn ein Benutzer Ihre Anwendung einem zusätzlichen Dateityp zuweist, hat dieser Typ diese Merkmale. Wenn der zusätzliche Dateityp zuvor einer anderen Anwendung zugeordnet war, ersetzen diese Merkmale die Originale.

Um die Standardprozedur zu registrieren, platzieren Sie die gleichen Registrierungsschlüssel, die Sie für die ProgID Ihrer Anwendung erstellt haben, unter dem Unterschlüssel der Anwendung von **HKEY \_ CLASSES \_ ROOT** \\ **Applications**. Sie können auch einen FriendlyAppName-Wert einschließen, um dem System einen Anzeigenamen für Ihre Anwendung bereitzustellen. Der Anzeigename der Anwendung kann auch aus der ausführbaren Datei extrahiert werden, jedoch nur, wenn der FriendlyAppName-Wert nicht vorhanden ist. Das folgende Registrierungsfragment zeigt eine Beispielstandardprozedur für MyProgram.exe, die einen Anzeigenamen und mehrere Kontextmenüelemente definiert. Die Befehlszeichenfolgen enthalten das Flag /a, um die Anwendung zu benachrichtigen, dass sie einen beliebigen Dateityp öffnet. Wenn Sie einen **DefaultIcon-Unterschlüssel** einschließen, sollten Sie ein generisches Symbol verwenden.

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

Wenn ein Benutzer das Menü **Datei** in Windows Explorer öffnet, lautet der erste Befehl **Neu.** Wenn Sie diesen Befehl auswählen, wird ein Untermenü angezeigt. Standardmäßig enthält sie die beiden Befehle **Ordner** und **Verknüpfung,** mit denen Benutzer Unterordner und Verknüpfungen erstellen können. Dieses Untermenü kann erweitert werden, um Dateierstellungsbefehle für jeden Dateityp einzuschließt.

Um dem Untermenü **New** einen Dateierstellungsbefehl hinzuzufügen, müssen den Dateien Ihrer Anwendung ein [Dateityp](fa-file-types.md) zugeordnet sein. Fügen Sie einen **ShellNew-Unterschlüssel** unter dem Schlüssel für die Dateinamenerweiterung ein. Wenn der Befehl **Neu** im Menü **Datei** ausgewählt ist, fügt die Shell ihn dem Untermenü **Neu** hinzu. Die Anzeigezeichenfolge des Befehls ist die beschreibende Zeichenfolge, die der ProgID des Programms zugewiesen ist.

Weisen Sie dem **ShellNew-Unterschlüssel** mindestens einen Datenwert zu, um die Dateierstellungsmethode anzugeben. Die verfügbaren Werte folgen.



| Wert    | BESCHREIBUNG                                                                                                                                                   |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Befehl  | Führt eine Anwendung aus. Dies ist ein **REG \_ SZ-Wert,** der den Pfad der auszuführenden Anwendung angibt. Sie können z. B. festlegen, dass ein Assistent gestartet wird. |
| Daten     | Erstellt eine Datei mit angegebenen Daten. Data ist ein **REG \_ BINARY-Wert** mit den Daten der Datei. Daten werden ignoriert, wenn entweder NULLFile oder FileName angegeben ist.  |
| FileName | Erstellt eine Datei, die eine Kopie einer angegebenen Datei ist. FileName ist ein **REG \_ SZ-Wert,** der auf den vollqualifizierten Pfad der zu kopierenden Datei festgelegt ist.                 |
| NULLFile | Erstellt eine leere Datei. NullFile wird kein Wert zugewiesen. Wenn NULLFile angegeben wird, werden die Werte Data und FileName ignoriert.                                  |



 

Die folgende Abbildung zeigt das **Neue** Untermenü für den .myp-Dateityp, der als Beispiel in [Dateitypen](fa-file-types.md) und [Anpassen von Symbolen](icon.md)verwendet wird. Sie verfügt jetzt über den Befehl **MyProgram Application**. Wenn ein Benutzer im Untermenü **Neu** die Option **MyProgram-Anwendung** auswählt, erstellt die Shell eine Datei mit dem Namen "New MyProgram Application.myp" und übergibt sie an MyProgram.exe.

![Screenshot des benutzerdefinierten neuen Menüs](images/context5.png)

Der Registrierungseintrag lautet jetzt wie folgt:

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

 

 



