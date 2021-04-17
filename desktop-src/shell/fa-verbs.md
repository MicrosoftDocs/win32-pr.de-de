---
description: Wenn ein Benutzer mit der rechten Maustaste auf ein Shellobjekt (z. b. eine Datei) klickt, zeigt die Shell ein Kontextmenü an.
ms.assetid: 4f46b8c3-1e12-447c-87f4-bbe2c305f77a
title: Verben und Dateizuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b398b168afe66c3ddd1abe4c78863fbf67ffcbd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559757"
---
# <a name="verbs-and-file-associations"></a>Verben und Dateizuordnungen

Wenn ein Benutzer mit der rechten Maustaste auf ein Shellobjekt (z. b. eine Datei) klickt, zeigt die Shell ein Kontextmenü an. Dieses Menü enthält eine Liste mit Befehlen, die der Benutzer auswählen kann, um verschiedene Aktionen für das Element auszuführen. Diese Befehle werden auch als Kontextmenü Elemente oder Verben bezeichnet. Kontextmenüs können angepasst werden.

Dieses Thema ist wie folgt organisiert:

-   [Einführung in Kontextmenüs für Datei System Objekte](#introduction-to-shortcut-menus-for-file-system-objects)
    -   [Hinzufügen von Befehlen zu einem Kontextmenü](#add-commands-to-a-shortcut-menu)
-   [Kontextmenü Verben](#shortcut-menu-verbs)
-   [Nicht-Datei System Elemente und OpenSearch-Ergebnisse streamen.](#stream-non-file-system-items-and-opensearch-results)
-   [Registrieren einer Anwendung, um beliebige Dateitypen zu verarbeiten](#register-an-application-to-handle-arbitrary-file-types)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction-to-shortcut-menus-for-file-system-objects"></a>Einführung in Kontextmenüs für Datei System Objekte

Da für die Dateiverwaltung häufig Kontextmenüs verwendet werden, stellt die Shell eine Reihe von Standard Befehlen (z. b. **Ausschneiden** und **Kopieren**) bereit, die im Kontextmenü für ein beliebiges Dateisystem Objekt, z. b. eine Datei oder einen Ordner, angezeigt werden.

Das folgende Beispiel veranschaulicht ein Standardkontext Menü, das angezeigt wird, wenn Sie mit der rechten Maustaste auf **MyFile.XYZ-MS** klicken.

![Screenshot des Standardkontext Menüs](images/context-menu/context-filesystemobjects.png)

Der Grund, warum ein Standardkontext Menü für **MyFile.XYZ-MS** angezeigt wird, ist darauf zurückzuführen, dass **. XYZ-MS** kein Member eines registrierten Dateityps ist. Im Gegensatz dazu ist " **. txt** " ein registrierter Dateityp. Wenn Sie mit der rechten Maustaste auf eine **txt** -Datei klicken, wird ein Kontextmenü mit drei zusätzlichen Befehlen im oberen Abschnitt angezeigt: **Drucken**, **Bearbeiten** und **Öffnen mit**.

![Screenshot des Kontextmenüs für eine Datei mit einem registrierten Dateityp](images/context-menu/context-registeredfiletype.png)

Um das Kontextmenü für einen Dateityp zu erweitern, müssen Sie für jeden Befehl einen Registrierungs Eintrag erstellen. Ein anspruchsvolleres Verfahren ist die Implementierung eines Kontextmenü-Handlers (Verb), mit dem Sie das Kontextmenü für einen Dateityp Datei-für-Datei-Basis erweitern können. Weitere Informationen finden Sie unter [Erstellen von Kontextmenü Handlern](context-menu-handlers.md)und [Kontextmenü Referenz](context-menu-reference.md).

### <a name="add-commands-to-a-shortcut-menu"></a>Hinzufügen von Befehlen zu einem Kontextmenü

Ein Kontextmenü Handler ist ein Dateityp Handler, der einem vorhandenen Kontextmenü Befehle hinzufügt. Kontextmenü Handler sind einem Dateityp zugeordnet und werden aufgerufen, wenn ein Kontextmenü für ein Member der Klasse angezeigt wird. Die Shell überprüft die Registrierung, um festzustellen, ob der Dateityp mit beliebigen Kontextmenü Handlern verknüpft ist. Wenn dies der Fall ist, fragt die Shell die Handler nach zusätzlichen Kontextmenü Elementen ab.

## <a name="shortcut-menu-verbs"></a>Kontextmenü Verben

Jeder Befehl im Kontextmenü wird durch sein Verb in der Registrierung identifiziert. Diese Verben sind identisch mit denen, die von [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) verwendet werden, wenn Anwendungen Programm gesteuert gestartet werden.

Ein Verb ist eine einfache Text Zeichenfolge, die von der Shell verwendet wird, um den zugehörigen Befehl zu identifizieren. Jedes Verb entspricht der Befehls Zeichenfolge, die verwendet wird, um den Befehl in einem Konsolenfenster oder einer Batchdatei (. bat) zu starten.

Beispielsweise wird im geöffneten Verb normalerweise ein Programm zum Öffnen einer Datei gestartet. Die Befehls Zeichenfolge sieht normalerweise wie folgt aus:


```
"My Program.exe" "%1"
```



Wenn ein beliebiges Element der Befehls Zeichenfolge Leerzeichen enthält, muss es in Anführungszeichen eingeschlossen werden. Wenn das Element ein Leerzeichen enthält, wird es andernfalls nicht ordnungsgemäß analysiert. Beispielsweise wird die Anwendung mit **"My Program.exe"** ordnungsgemäß gestartet. Wenn Sie **meine Program.exe** ohne Anführungszeichen verwenden, versucht das System, " **My** " mit **Program.exe** als erstes Befehlszeilenargument zu starten. Sie sollten immer Anführungszeichen mit Argumenten wie **"%1**" verwenden, die von der Shell auf Zeichen folgen erweitert werden, da Sie nicht sicher sein können, dass die Zeichenfolge kein Leerzeichen enthält.

Verben können auch ein angeordneter Anzeige Name zugeordnet werden, der im Kontextmenü anstelle der Verb Zeichenfolge selbst angezeigt wird. Beispielsweise ist die Anzeige Zeichenfolge für openas **mit geöffnet**. Wie normale Menü Zeichenfolgen, einschließlich eines kaufmännischen und-Zeichens in der Anzeige Zeichenfolge, wird die Tastaturauswahl des Befehls ermöglicht.

## <a name="stream-non-file-system-items-and-opensearch-results"></a>Nicht-Datei System Elemente und OpenSearch-Ergebnisse streamen.

In Windows 7 und höher wird die Verbindung externer Quellen mit dem Windows-Client über das [OpenSearch](http://www.opensearch.org/) -Protokoll unterstützt. Dies ermöglicht es Benutzern, in Windows-Explorer einen Remote Datenspeicher zu durchsuchen und Ergebnisse anzuzeigen. Der Standard OpenSearch v 1.1 definiert einfache Dateiformate, die verwendet werden können, um zu beschreiben, wie ein Client den Webdienst für den Datenspeicher Abfragen soll und wie der Dienst Ergebnisse zurückgeben soll, die vom Client gerendert werden sollen.

Möglicherweise müssen Sie nicht Dateisystem Elemente streamen, um zu vermeiden, dass Elemente im Fall von [OpenSearch](http://www.opensearch.org/) -Ergebnissen heruntergeladen werden müssen. Die Funktion für die Verbund Suche ermöglicht das Suchen von Elementen aus nicht-Dateisystem Standorten, die OpenSearch unterstützen, z. b. SharePoint und andere Webdienste-gestützte Websites. Wenn Sie Verben für diese Elemente aufrufen, lädt das System eine temporäre Version des Elements herunter und übergibt sie an die Verb-Implementierung. Verb Implementierer wird empfohlen, die Datei nicht herunterzuladen, indem Sie den Satz von URL-Schemas registrieren, den das Verb unterstützt, um die Elemente zu streamen. Verben verwenden dazu den **supportedprotokolls** -Registrierungsschlüssel.

## <a name="register-an-application-to-handle-arbitrary-file-types"></a>Registrieren einer Anwendung, um beliebige Dateitypen zu verarbeiten

Wenn Sie Kontextmenü Elemente für einen bestimmten Dateityp definieren, können Sie angeben, wie die zugehörige Anwendung einen Member des Dateityps öffnet. Anwendungen können jedoch auch eine separate Standardprozedur registrieren, die verwendet wird, wenn ein Benutzer versucht, die Anwendung zu verwenden, um einen Dateityp zu öffnen, der nicht der Anwendung zugeordnet ist. Sie registrieren das Standardverfahren ähnlich wie beim Registrieren von Kontextmenü Elementen. Ausführlichere Informationen zum Definieren von Kontextmenü Elementen finden Sie unter [Erstellen von Kontextmenü Handlern](context-menu.md).

Die Standardprozedur dient zwei grundlegenden Zwecken. Eine besteht darin, anzugeben, wie die Anwendung aufgerufen werden soll, um einen beliebigen Dateityp zu öffnen. Beispielsweise können Sie ein befehlszeilenflag verwenden, um anzugeben, dass ein Unbekannter Dateityp geöffnet wird. Der andere Zweck besteht darin, die verschiedenen Merkmale eines Dateityps zu definieren, z. b. die Kontextmenü Elemente und das Symbol. Wenn ein Benutzer die Anwendung einem zusätzlichen Dateityp zuordnet, hat diese Klasse diese Merkmale. Wenn der zusätzliche Dateityp zuvor mit einer anderen Anwendung verknüpft war, werden die Original Eigenschaften durch diese Merkmale ersetzt.

Um die Standardprozedur zu registrieren, platzieren Sie die gleichen Registrierungsschlüssel, die Sie für die ProgID Ihrer Anwendung erstellt haben, unter dem Unterschlüssel der Anwendung von **HKEY \_ Classes \_ root \\ Applications**. Sie können auch einen **friendlyappname** -Wert einschließen, um dem System einen anzeigen Amen für die Anwendung bereitzustellen. Der Anzeige Name der Anwendung kann auch aus der ausführbaren Datei extrahiert werden, jedoch nur, wenn der friendlyappname-Wert nicht vorhanden ist.

Der folgende Beispiel Registrierungs Eintrag veranschaulicht eine Standardprozedur für **MyProgram.exe** , die einen anzeigen Amen und mehrere Kontextmenü Elemente definiert. Die Befehls Zeichenfolgen enthalten das Flag **/a** , um die Anwendung darüber zu benachrichtigen, dass ein beliebiger Dateityp geöffnet wird. Wenn Sie einen **DefaultIcon** -Unterschlüssel einschließen, sollten Sie ein generisches Symbol verwenden.

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

-   Weitere Hintergrundinformationen finden [Sie unter Einführung in Dateizuordnungen](fa-intro.md).
-   Konzeptionelle Informationen zum Erweitern der Shell mit Dateityp Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Kontextmenü Handler und Mehrfachauswahl Verben](verbs-best-practices.md)
</dt> <dt>

[Auswählen eines statischen oder dynamischen Verbs für das Kontextmenü](shortcut-choose-method.md)
</dt> <dt>

[Erstellen von Kontextmenü Handlern](context-menu-handlers.md)
</dt> <dt>

[Anpassen eines Kontextmenüs mithilfe dynamischer Verben](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Kontextmenüs und Kontextmenü Handler](context-menu.md)
</dt> <dt>

[Verweis auf das Kontextmenü](context-menu-reference.md)
</dt> </dl>

 

 



