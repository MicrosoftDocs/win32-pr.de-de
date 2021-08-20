---
description: Wenn ein Benutzer mit der rechten Maustaste auf ein Shell-Objekt klickt, z. B. eine Datei, zeigt die Shell ein Kontextmenü an.
ms.assetid: 4f46b8c3-1e12-447c-87f4-bbe2c305f77a
title: Verben und Dateizuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a144051b04ef2d9a2c9877b53e1680d4274afc92d3fc87fbcb531b02a0f94946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860787"
---
# <a name="verbs-and-file-associations"></a>Verben und Dateizuordnungen

Wenn ein Benutzer mit der rechten Maustaste auf ein Shell-Objekt klickt, z. B. eine Datei, zeigt die Shell ein Kontextmenü an. Dieses Menü enthält eine Liste von Befehlen, die der Benutzer auswählen kann, um verschiedene Aktionen für das Element auszuführen. Diese Befehle werden auch als Kontextmenüelemente oder Verben bezeichnet. Kontextmenüs können angepasst werden.

Dieses Thema ist wie folgt organisiert:

-   [Einführung in Kontextmenüs für Dateisystemobjekte](#introduction-to-shortcut-menus-for-file-system-objects)
    -   [Hinzufügen von Befehlen zu einem Kontextmenü](#add-commands-to-a-shortcut-menu)
-   [Kontextmenüverben](#shortcut-menu-verbs)
-   [Streamen Sie Nichtdateisystemelemente, und OpenSearch Ergebnisse.](#stream-non-file-system-items-and-opensearch-results)
-   [Registrieren einer Anwendung zur Handhabung beliebiger Dateitypen](#register-an-application-to-handle-arbitrary-file-types)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction-to-shortcut-menus-for-file-system-objects"></a>Einführung in Kontextmenüs für Dateisystemobjekte

Da Kontextmenüs häufig für die Dateiverwaltung verwendet werden, stellt  die Shell eine Reihe von Standardbefehlen wie Ausschneiden und Kopieren zur Auswahl, die im Kontextmenü für jedes Dateisystemobjekt wie eine Datei oder einen Ordner angezeigt werden.

Das folgende Beispiel veranschaulicht ein Standardverknüpfungsmenü, das angezeigt wird, indem Sie mit der rechten Maustaste **MyFile.xyz-ms klicken.**

![Screenshot des Standardverknüpfungsmenüs](images/context-menu/context-filesystemobjects.png)

Der Grund dafür, dass für **MyFile.xyz-ms ein** Standardverknüpfungsmenü angezeigt wird, liegt daran, dass **.xyz-ms** kein Member eines registrierten Dateityps ist. Im Gegensatz dazu **ist.txt** ein registrierter Dateityp. Wenn Sie mit der rechten **Maustaste** auf eine.txtklicken, wird im oberen Abschnitt ein  Kontextmenü mit drei zusätzlichen Befehlen **angezeigt:** **Drucken,** Bearbeiten und Öffnen mit .

![Screenshot des Kontextmenüs für eine Datei mit einem registrierten Dateityp](images/context-menu/context-registeredfiletype.png)

Um das Kontextmenü für einen Dateityp zu erweitern, müssen Sie für jeden Befehl einen Registrierungseintrag erstellen. Ein komplexerer Ansatz ist die Implementierung eines Handlers für Kontextmenüs (Verben), mit dem Sie das Kontextmenü für einen Dateityp dateispezifische erweitern können. Weitere Informationen finden Sie unter [Erstellen von Kontextmenühandlern](context-menu-handlers.md)und [Kontextmenüreferenz.](context-menu-reference.md)

### <a name="add-commands-to-a-shortcut-menu"></a>Hinzufügen von Befehlen zu einem Kontextmenü

Ein Kontextmenühandler ist ein Dateityphandler, der einem vorhandenen Kontextmenü Befehle hinzufügt. Kontextmenühandler sind einem Dateityp zugeordnet und werden aufgerufen, wenn ein Kontextmenü für einen Member der -Klasse angezeigt wird. Die Shell überprüft die Registrierung, um zu prüfen, ob der Dateityp einem Kontextmenühandler zugeordnet ist. Wenn dies der Fehler ist, fragt die Shell die Handler nach zusätzlichen Kontextmenüelementen ab.

## <a name="shortcut-menu-verbs"></a>Kontextmenüverben

Jeder Befehl im Kontextmenü wird in der Registrierung anhand seines Verbs identifiziert. Diese Verben sind identisch mit denen, die von [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) beim programmgesteuerten Starten von Anwendungen verwendet werden.

Ein Verb ist eine einfache Textzeichenfolge, die von der Shell verwendet wird, um den zugeordneten Befehl zu identifizieren. Jedes Verb entspricht der Befehlszeichenfolge, die zum Starten des Befehls in einem Konsolenfenster oder einer Batchdatei (.bat wird.

Beispielsweise startet das geöffnete Verb normalerweise ein Programm, um eine Datei zu öffnen. Die Befehlszeichenfolge sieht in der Regel wie folgt aus:


```
"My Program.exe" "%1"
```



Wenn ein Element der Befehlszeichenfolge Leerzeichen enthält oder enthalten kann, muss es in Anführungszeichen eingeschlossen werden. Andernfalls wird das Element nicht ordnungsgemäß analysiert, wenn es ein Leerzeichen enthält. Beispielsweise startet **"My Program.exe"** die Anwendung ordnungsgemäß. Wenn Sie My Program.exeohne **Anführungszeichen** verwenden, versucht  das System, My mit **Program.exe** als erstes Befehlszeilenargument zu starten. Sie sollten immer Anführungszeichen mit Argumenten wie **"%1"** verwenden, die von der Shell auf Zeichenfolgen erweitert werden, da Sie nicht sicher sein können, dass die Zeichenfolge kein Leerzeichen enthält.

Verben kann auch ein Anzeigename zugeordnet sein, der im Kontextmenü anstelle der Verbzeichenfolge selbst angezeigt wird. Die Anzeigezeichenfolge für openas ist z. B. **Open With**. Wie normale Menüzeichenfolgen ermöglicht auch das Hinzufügen eines ampersand-Zeichens in die Anzeigezeichenfolge die Tastaturauswahl des Befehls.

## <a name="stream-non-file-system-items-and-opensearch-results"></a>Streamen von Nichtdateisystemelementen und OpenSearch Ergebnisse.

In Windows 7 und höher wird die Verbindung externer Quellen mit dem Windows-Client über das OpenSearch [unterstützt.](http://www.opensearch.org/) Dadurch können Benutzer einen Remotedatenspeicher durchsuchen und Ergebnisse aus dem Windows anzeigen. Der OpenSearch v1.1-Standard definiert einfache Dateiformate, die verwendet werden können, um zu beschreiben, wie ein Client den Webdienst nach dem Datenspeicher abfragen soll und wie der Dienst Ergebnisse zurückgeben soll, die vom Client gerendert werden sollen.

Möglicherweise müssen Sie Nicht-Dateisystemelemente streamen, um zu vermeiden, dass Elemente heruntergeladen werden müssen, wenn OpenSearch [werden.](http://www.opensearch.org/) Die Verbundsuchfunktion ermöglicht das Durchsuchen von Elementen von Speicherorten, die keine Dateisysteme sind, die OpenSearch unterstützen, z. B. SharePoint und andere websites, die von Webdiensten unterstützt werden. Beim Aufrufen von Verben für diese Elemente lädt das System eine temporäre Version des Elements herunter und übergibt sie an die Verbimplementierung. Verb-Implementierern wird empfohlen, das Herunterladen der Datei zu vermeiden, indem der Satz von URL-Schemas registriert wird, die das Verb zum Streamen der Elemente unterstützt. Verben verwenden dazu den **Registrierungsschlüssel SupportedProtocols.**

## <a name="register-an-application-to-handle-arbitrary-file-types"></a>Registrieren einer Anwendung zur Handhabung beliebiger Dateitypen

Durch das Definieren von Kontextmenüelementen für einen bestimmten Dateityp können Sie angeben, wie die zugeordnete Anwendung einen Member des Dateityps öffnet. Anwendungen können jedoch auch eine separate Standardprozedur registrieren, die verwendet wird, wenn ein Benutzer versucht, die Anwendung zum Öffnen eines Dateityps zu verwenden, der nicht der Anwendung zugeordnet ist. Sie registrieren die Standardprozedur auf die gleiche Weise wie Kontextmenüelemente. Ausführlichere Informationen zum Definieren von Kontextmenüelementen finden Sie unter [Erstellen von Kontextmenühandlern.](context-menu.md)

Die Standardprozedur dient zwei grundlegenden Zwecken. Eine besteht in der Angabe, wie Ihre Anwendung aufgerufen werden soll, um einen beliebigen Dateityp zu öffnen. Sie können beispielsweise ein Befehlszeilenflag verwenden, um anzugeben, dass ein unbekannter Dateityp geöffnet wird. Der andere Zweck besteht im Definieren der verschiedenen Merkmale eines Dateityps, z. B. der Kontextmenüelemente und des Symbols. Wenn ein Benutzer Ihre Anwendung einem zusätzlichen Dateityp zuweist, hat diese Klasse diese Merkmale. Wenn der zusätzliche Dateityp zuvor einer anderen Anwendung zugeordnet war, ersetzen diese Merkmale die Originale.

Um die Standardprozedur zu registrieren, platzieren Sie dieselben Registrierungsschlüssel, die Sie für die ProgID Ihrer Anwendung erstellt haben, unter dem Unterschlüssel der Anwendung **von HKEY \_ CLASSES ROOT \_ \\ Applications**. Sie können auch einen **FriendlyAppName-Wert** angeben, um dem System einen Benutzerfreundlichen Namen für Ihre Anwendung zu geben. Der Angezeigte Name der Anwendung kann auch aus der ausführbaren Datei extrahiert werden, jedoch nur, wenn der FriendlyAppName-Wert nicht vorhanden ist.

Der folgende Beispielregistrierungseintrag veranschaulicht  eine Standardprozedur fürMyProgram.exe, die einen Benutzernamen und mehrere Kontextmenüelemente definiert. Die Befehlszeichenfolgen enthalten das **Flag /a,** um die Anwendung zu benachrichtigen, dass sie einen beliebigen Dateityp öffnet. Wenn Sie einen **DefaultIcon-Unterschlüssel** enthalten, sollten Sie ein generisches Symbol verwenden.

```
HKEY_CLASSES_ROOT
   MyProgram.exe
      shell
         open
            command
               (Default) = C:\MyDir\MyProgram.exe /a "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2"
```

## <a name="additional-resources"></a>Weitere Ressourcen

-   Weitere Hintergrundinformationen finden Sie unter [Einführung in Dateizuordnungen.](fa-intro.md)
-   Konzeptionelle Informationen zum Erweitern der Shell mit Dateityphandlern finden Sie unter [Creating Shell Extension Handlers](handlers.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Kontextmenühandler und Mehrfachauswahlverben](verbs-best-practices.md)
</dt> <dt>

[Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü](shortcut-choose-method.md)
</dt> <dt>

[Erstellen von Kontextmenühandlern](context-menu-handlers.md)
</dt> <dt>

[Anpassen eines Kontextmenüs mit dynamischen Verben](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Kontextmenüs und Kontextmenühandler](context-menu.md)
</dt> <dt>

[Kontextmenüreferenz](context-menu-reference.md)
</dt> </dl>

 

 



