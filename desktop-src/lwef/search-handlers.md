---
title: Erstellen von Such Handlern
description: Die Shell unterstützt mehrere Such Dienstprogramme, die Benutzern das Auffinden von Namespace Objekten wie Dateien oder Druckern ermöglichen. Sie können eine benutzerdefinierte Such-Engine erstellen und für Benutzer verfügbar machen, indem Sie einen Such Handler implementieren und registrieren.
ms.assetid: ffd023bb-16ab-43ce-b00b-5e32656c8013
keywords:
- Such Handler
- registrieren, Durchsuchen von Handlern
- statische Such Handler
- registrieren, statische Such Handler
- dynamische Such Handler
- registrieren, dynamische Such Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6476109302a176822137747353b2762b0caea8a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315033"
---
# <a name="creating-search-handlers"></a>Erstellen von Such Handlern

\[Dieses Feature wird nur unter Windows XP oder früher unterstützt. Verwenden Sie stattdessen die Windows-Suche.\]

Die Shell unterstützt mehrere Such Dienstprogramme, die Benutzern das Auffinden von Namespace Objekten wie Dateien oder Druckern ermöglichen. Sie können eine benutzerdefinierte Such-Engine erstellen und für Benutzer verfügbar machen, indem Sie einen *Such Handler* implementieren und registrieren.

Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shellerweiterungs Handlers werden unter [Erstellen von Shellerweiterungs Handlern](/windows/desktop/shell/handlers)erläutert. Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die für Such Handler spezifisch sind.

-   [Funktionsweise von Such Handlern](#how-search-handlers-work)
-   [Registrieren von Such Handlern](#registering-search-handlers)
    -   [Registrieren eines statischen Such Handlers](#registering-a-static-search-handler)
    -   [Registrieren eines dynamischen Such Handlers](#registering-a-dynamic-search-handler)
-   [Implementieren von Such Handlern](#implementing-search-handlers)

## <a name="how-search-handlers-work"></a>Funktionsweise von Such Handlern

Benutzer haben zwei Möglichkeiten, eine Suchmaschine auszuwählen. Die erste Möglichkeit ist das Startmenü. Mit Systemen vor Windows 2000 wird durch Auswählen des **Befehls Suchen im** **Startmenü** ein Untermenü der verfügbaren Suchmaschinen angezeigt. Bei Windows 2000 und höher wird **der Befehl Suchen im** **St**-Art-Menü in suchen umbenannt. Die folgende Abbildung zeigt die **Such** Schaltfläche auf einem Windows XP-System.

![Das suchuntermenü des Startmenüs](images/searchhandler1.jpg)

Benutzer können auch eine Suche in Windows-Explorer starten. Auf Systemen, die älter als Windows 2000 sind, klicken Sie auf den Befehl **Suchen** **im Menü Extras** , um im Wesentlichen das gleiche Menü wie das, das dem **Startmenü** zugeordnet ist, anzuzeigen. Windows Explorer für Windows 2000 verarbeitet Suchmaschinen jedoch auf eine ganz andere Weise. Anstatt Suchmaschinen als Untermenü des Menüs Extras zu behandeln, gibt es jetzt eine **Such** Schaltfläche **auf der Symbol** Leiste. Durch Klicken auf diese Schaltfläche wird der **Such** Bereich der Explorer-Leiste geöffnet. Die folgende Abbildung zeigt den Suchbereich **für Dateien und Ordner suchen** .

![der Suchbereich der Windows-Explorer-Leiste](images/searchhandler2.jpg)

Es gibt eine Reihe von Unterschieden in der Art und Weise, wie Windows 2000 und frühere Systeme Such Handler verwalten, die sowohl die Implementierung als auch die Registrierung beeinflussen.



| Vor Windows 2000                                                                                                                                                                                                       | Windows 2000 und höher                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Such Handler werden als Typ eines Kontext [Menü Handler](/windows/desktop/shell/context-menu-handlers)implementiert.                                                                                                                     | Such Handler können als Kontextmenü Handler oder als dynamische HTML (DHTML)-Dokumente implementiert werden.                                                                                                                                                                                                               |
| Such Handler können statisch oder dynamisch sein. Statische Handler werden nur geladen, wenn Sie vom Benutzer ausgewählt werden. Dynamische Handler werden beim Start von der Shell geladen und erst beendet, wenn die Shell beendet wird. | Handler, die als Kontextmenü Handler implementiert werden, können entweder statisch oder dynamisch sein. Handler, die als DHTML-Dokumente implementiert werden, müssen statisch sein.                                                                                                                                                                           |
| Such Handler werden im Menü " **Suchen"** im Menü " **Start** " **und im Menü "suchen"** im Menü "Extras" von  **Windows Explorer angezeigt** .                                                                                  | Such Handler werden nur im Untermenü **Suchen** im **Startmenü** angezeigt. Um einen benutzerdefinierten Suchbereich über die Windows Explorer-Menüleiste verfügbar zu machen, müssen Sie ihn als [Band Objekt](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85))implementieren. Er wird dann im Untermenü der **Explorer-Leiste** des Windows-Explorer- **Ansichts** Menüs aufgeführt. |



 

## <a name="registering-search-handlers"></a>Registrieren von Such Handlern

Such Handler werden unter dem **findextensions**-Unterschlüssel des Datei Typs registriert.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

An diesem Punkt hängt das Registrierungsverfahren davon ab, ob der Handler statisch oder dynamisch ist. Eine allgemeine Erläuterung zum Registrieren von Shellerweiterungs Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](/windows/desktop/shell/handlers).

### <a name="registering-a-static-search-handler"></a>Registrieren eines statischen Such Handlers

Statische Such Handler werden nur geladen, wenn Sie vom Benutzer gestartet werden. Diese Vorgehensweise funktioniert am besten für DLLs, die klein sind und schnell geladen werden können. Wenn Sie DHTML verwenden, um den Handler zu implementieren, muss er statisch sein. Um einen statischen Erweiterungs Handler zu registrieren, erstellen Sie einen Unterschlüssel mit dem Namen für den Handler unter dem **statischen** Unterschlüssel des **findextensions** -unter Schlüssels. Der Name wird nicht vom System verwendet, er darf jedoch nicht mit anderen suchhandlernamen unter dem **findextensions** -Unterschlüssel identisch sein.

### <a name="shortcut-menu-based-search-handlers"></a>Kontextmenü basierte Such Handler

Wenn der Handler als Kontext [Menü Handler](/windows/desktop/shell/context-menu-handlers)implementiert ist, legen Sie den Standardwert des Namens unter Schlüssels des Handlers auf die Klassen-ID des-Objekts (CLSID) des Objekts fest. Erstellen Sie unter dem namens Unterschlüssel des Handlers einen Unterschlüssel mit dem Namen **0**   (null), und legen Sie dessen Standardwert auf die Zeichenfolge fest,  die im Untermenü **Suchen oder suchen** angezeigt wird. Sie können Tastenkombinationen auf die übliche Weise aktivieren, indem Sie das Tastenkombination mit einem kaufmännischen und-Zeichen (&) vorangestellt werden. Sie können ein optionales kleines Symbol rechts neben dem Menütext anzeigen, indem Sie einen **DefaultIcon** -Unterschlüssel unter dem **0** -Unterschlüssel erstellen. Legen Sie den Standardwert auf eine Zeichenfolge fest, die den Pfad der Datei enthält, die das Symbol enthält, gefolgt von einem Komma, gefolgt vom Null basierten Index des Symbols.

Im folgenden Beispiel wird der Such Handler **mysearchengine** registriert. Der Menütext lautet "meine Suchmaschine", wobei M als Tastenkombination angegeben ist. Das Symbol befindet sich in C: \\ mydir \\MySearch.dll mit einem Index von 2.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {MySearchEngine CLSID GUID}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
```

### <a name="dhtml-based-search-handlers"></a>DHTML-basierte Such Handler

Mit Windows 2000 können Sie auch einen Such Handler als DHTML-Dokument implementieren. Der Name wird im Untermenü **Suchen** im **Startmenü** aufgeführt. Wenn der Benutzer das Symbol auswählt, wird Windows-Explorer gestartet, und die Explorer-Leiste wird für das Such Dokument geöffnet. Sie können auch ein DHTML-Dokument angeben, das rechts neben der Explorer-Leiste angezeigt werden soll. Es gibt keine Möglichkeit, einen anderen Handler aus dem Standard Suchbereich zu starten. Suchmaschinen können direkt aus dem Windows-Explorer gestartet werden, jedoch nur, wenn Sie als [Band Objekte](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85))implementiert werden.

Legen Sie zum Registrieren eines DHTML-basierten Such Handlers den namens Unterschlüssel des Handlers auf die Zeichen folgen Form von CLSID \_ shellsearchext fest (aktuell {169 a0691-8df9-11d1-a1c4-00c04fd75d13}), und erstellen Sie die folgenden Unterschlüssel.

1.  Erstellen Sie den Unterschlüssel " **0**" (null) unter dem Unterschlüssel "HandlerName", und legen Sie dessen Standardwert auf den Menütext fest.
2.  Wenn neben dem Menütext ein Symbol angezeigt werden soll, erstellen Sie einen **DefaultIcon** -Unterschlüssel unter **0** , und legen Sie dessen Standardwert auf den Pfad und den Index des Symbols fest.
3.  Erstellen Sie den Unterschlüssel " **searchguid** " unter **0**. Weisen Sie dem DHTML-Dokument eine GUID zu, und legen Sie den Standardwert von **searchguid** auf das zugehörige Zeichen folgen Formular fest. Diese GUID muss nicht unter **HKEY \_ Classes \_ root \\ CLSID** registriert werden.
4.  Erstellen Sie unter **searchguid** einen **URL** -Unterschlüssel. Legen Sie den Standardwert auf den Pfad des HTML-Dokuments fest, das in der Explorer-Leiste angezeigt wird.
5.  Erstellen Sie unter " **searchguid**" einen **urlnavnew** -Unterschlüssel. Legen Sie den Standardwert auf den Pfad des HTML-Dokuments fest, das rechts neben der Explorer-Leiste angezeigt wird.

Im folgenden Beispiel wird der als DHTML-Dokument implementierte **mysearchengine** -Such Handler registriert. Der Menütext lautet "meine Suchmaschine", wobei M als Tastenkombination angegeben ist. Das Symbol befindet sich in C: \\ mydir \\MySearch.dll mit einem Index von 2. Das DHTML-Dokument der Explorer-Leiste ist c: \\ mydir \\MySearch.htm, und das Dokument, das rechts von der Explorer-Leiste angezeigt wird, ist c: \\ mydir \\MySearchPage.htm.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {169A0691-8DF9-11d1-A1C4-00C04FD75D13}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
                                 SearchGUID
                                    (Default) = {My Search GUID}
                                    Url
                                       (Default) = C:\MyDir\MySearch.htm
                                    UrlNavNew
                                       (Default) = C:\MyDir\MySearchPage.htm
```

### <a name="registering-a-dynamic-search-handler"></a>Registrieren eines dynamischen Such Handlers

Wenn der Handler als Kontext [Menü Handler](/windows/desktop/shell/context-menu-handlers)implementiert ist, können Sie ihn auch als dynamischen Handler registrieren. In diesem Fall wird Sie mit der Shell geladen und wird nur beendet, wenn die Shell beendet wird. Dynamische Such Handler reagieren viel schneller als statische Handler, wenn Sie vom Benutzer gestartet werden. Diese Vorgehensweise funktioniert am besten, wenn die dll Ihres Handlers viel Zeit in Anspruch nehmen kann, oder wenn Sie wahrscheinlich häufig aufgerufen wird.

Dynamische Such Handler werden unter dem **findextensions** -Unterschlüssel registriert.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

Erstellen Sie einen Unterschlüssel von **findextensions** mit dem Namen für den Handler, und legen Sie dessen Standardwert auf die CLSID-GUID des Handlers fest. Menü Symbole werden für dynamische Such Handler nicht unterstützt. Im folgenden Beispiel wird mysearchengine als dynamischer Such Handler registriert.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     MySearchEngine
                        (Default) = {MySearchEngine CLSID GUID}
                        0
                           (Default) = &My Search Engine
```

Im Unterschied zu statischen Such Handlern geben Sie den Menütext nicht in der Registrierung an. Wenn der Handler geladen wird, ruft die **Shell die** [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) -Methode des Handlers auf, um dem Untermenü suchen oder **Suchen** Elemente hinzuzufügen.

## <a name="implementing-search-handlers"></a>Implementieren von Such Handlern

Such Handler können als Kontextmenü Handler für alle Versionen von Windows implementiert werden. Für Windows 2000 können diese auch als DHTML-Dokumente implementiert werden.

Eine allgemeine Erörterung der Implementierung von Kontextmenü Handlern finden Sie unter [Erstellen von Kontextmenü Handlern](/windows/desktop/shell/context-menu-handlers). Such Handler unterscheiden sich von standardmäßigen Kontextmenü Handlern in wenigen Punkten.

Bei statischen Menü Handlern wird das Untermenü **Suchen oder** **Suchen** aus den Informationen in der Registrierung erstellt. Es ist nicht erforderlich, dass der Handler ein Menü Element hinzufügt, da es sich dabei um einen normalen Kontextmenü Handler handelt. Die Shell verwaltet statische Menü Handler wie folgt.

-   Wenn der Benutzer das Menü Element des Handlers startet, lädt die Shell die DLL des Handlers und ruft [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) auf, um den Handler zu benachrichtigen, dass die Such-Engine gestartet wird. Die [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -und [**IContextMenu:: querycontextmenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) -Methoden werden nicht aufgerufen.
-   Wenn [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) aufgerufen wird, identifiziert der **lpverb** -Member der [**cminvokecommandinfo**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) -Struktur, die übergeben wird, den Befehl. Das nieder wertige Wort von **lpverb** wird auf die numerische Entsprechung des Unterschlüssel namens des Befehls festgelegt. Da dieser Unterschlüssel normalerweise den Namen **0** hat, wird **lpverb** normalerweise auf NULL festgelegt. Der Handler sollte dann die Suchmaschine starten.

Dynamische Such Handler werden ähnlich wie normale Kontextmenü Handler implementiert. Die primäre Ausnahme besteht darin, dass beim Aufrufen von [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) die Argumente *pidlfolder* und *lpdobj* auf **null** festgelegt werden.

DHTML-basierte Such Handler werden als normales DHTML-Dokument implementiert. Sie können beliebige HTML-, DHTML-oder Skript Erstellungs Technologien enthalten, die von Windows Internet Explorer unterstützt werden.

 

 