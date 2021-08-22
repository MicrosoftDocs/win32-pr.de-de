---
title: Erstellen von Suchhandlern
description: Die Shell unterstützt mehrere Suchprogramme, mit denen Benutzer Namespaceobjekte wie Dateien oder Drucker suchen können. Sie können eine benutzerdefinierte Suchmaschine erstellen und benutzern zur Verfügung stellen, indem Sie einen Suchhandler implementieren und registrieren.
ms.assetid: ffd023bb-16ab-43ce-b00b-5e32656c8013
keywords:
- Suchhandler
- Register, Suchhandler
- Statische Suchhandler
- Register, statische Suchhandler
- Dynamische Suchhandler
- Register, dynamische Suchhandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be891247c36687b0305e7e9c60711a233fb9b1d4f7f8554d0103be4cc0dc5a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975778"
---
# <a name="creating-search-handlers"></a>Erstellen von Suchhandlern

\[Dieses Feature wird nur unter Windows XP oder früher unterstützt. Verwenden Sie stattdessen Windows Search.\]

Die Shell unterstützt mehrere Suchprogramme, mit denen Benutzer Namespaceobjekte wie Dateien oder Drucker suchen können. Sie können eine benutzerdefinierte Suchmaschine erstellen und benutzern zur Verfügung stellen, indem Sie einen *Suchhandler* implementieren und registrieren.

Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shellerweiterungshandlers werden unter [Erstellen von Shellerweiterungshandlern](/windows/desktop/shell/handlers)erläutert. Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die spezifisch für Suchhandler sind.

-   [Funktionsweise von Suchhandlern](#how-search-handlers-work)
-   [Registrieren von Suchhandlern](#registering-search-handlers)
    -   [Registrieren eines statischen Suchhandlers](#registering-a-static-search-handler)
    -   [Registrieren eines dynamischen Suchhandlers](#registering-a-dynamic-search-handler)
-   [Implementieren von Suchhandlern](#implementing-search-handlers)

## <a name="how-search-handlers-work"></a>Funktionsweise von Suchhandlern

Benutzer haben zwei Möglichkeiten, eine Suchmaschine auszuwählen. Die erste Möglichkeit ist die Startmenü. Bei Systemen vor Windows 2000 wird durch Auswählen des Befehls **Suchen** im **Startmenü** ein Untermenü der verfügbaren Suchmaschinen angezeigt. Mit Windows 2000 und höher wird der Befehl **Suchen** des **Menüs St** art in Suchen umbenannt. Die folgende Abbildung zeigt die Schaltfläche **Suchen** auf einem Windows XP-System.

![Das Suchuntermenü des Startmenüs](images/searchhandler1.jpg)

Benutzer können eine Suche auch über Windows Explorer starten. Auf Systemen vor Windows 2000 klicken sie im Menü **Extras** auf den Befehl **Suchen,** um im Wesentlichen das gleiche Menü wie im **Startmenü** anzuzeigen. Allerdings verarbeitet Windows Explorer für Windows 2000 Suchmaschinen auf eine sehr andere Weise. Anstatt Suchmaschinen als Untermenü des Menüs **Extras** zu behandeln, gibt es jetzt **eine** Suchschaltfläche auf der Symbolleiste. Wenn Sie auf diese Schaltfläche klicken, wird der **Suchbereich** der Explorer-Leiste geöffnet. Die folgende Abbildung zeigt den Suchbereich **Nach Dateien und Ordnern** suchen.

![Suchbereich der Windows-Explorer-Leiste](images/searchhandler2.jpg)

Es gibt eine Reihe von Unterschieden bei der Verwaltung von Suchhandlern durch Windows 2000 und frühere Systeme, die sich sowohl auf die Implementierung als auch auf die Registrierung auswirken.



| Pre-Windows 2000                                                                                                                                                                                                       | Windows 2000 und höher                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Suchhandler werden als Typ des [Kontextmenühandlers](/windows/desktop/shell/context-menu-handlers)implementiert.                                                                                                                     | Suchhandler können als Kontextmenühandler oder als DHTML-Dokumente (Dynamic HTML) implementiert werden.                                                                                                                                                                                                               |
| Suchhandler können entweder statisch oder dynamisch sein. Statische Handler werden nur geladen, wenn sie vom Benutzer ausgewählt werden. Dynamische Handler werden beim Start von der Shell geladen und erst beendet, wenn die Shell beendet wird. | Handler, die als Kontextmenühandler implementiert werden, können entweder statisch oder dynamisch sein. Handler, die als DHTML-Dokumente implementiert werden, müssen statisch sein.                                                                                                                                                                           |
| Suchhandler werden im Untermenü **Suchen** des **Startmenüs** und im Untermenü **Suchen** des Menüs Windows **Explorer-Tools** angezeigt.                                                                                  | Suchhandler werden nur im Untermenü **Suchen** des **Startmenüs** angezeigt. Um einen benutzerdefinierten Suchbereich über die Windows Explorer-Menüleiste verfügbar zu machen, müssen Sie ihn als [Bandobjekt](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85))implementieren. Sie wird dann im Untermenü **Explorer-Leiste** des menüs Windows **Explorer-Ansicht** aufgeführt. |



 

## <a name="registering-search-handlers"></a>Registrieren von Suchhandlern

Suchhandler werden unter dem Unterschlüssel **FindExtensions** der Dateitypen registriert.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

Ab diesem Zeitpunkt hängt die Registrierungsprozedur davon ab, ob der Handler statisch oder dynamisch sein soll. Eine allgemeine Erläuterung zum Registrieren von Shellerweiterungshandlern finden Sie unter [Erstellen von Shellerweiterungshandlern.](/windows/desktop/shell/handlers)

### <a name="registering-a-static-search-handler"></a>Registrieren eines statischen Suchhandlers

Statische Suchhandler werden nur geladen, wenn sie vom Benutzer gestartet werden. Dieser Ansatz funktioniert am besten für DLLs, die klein sind und schnell geladen werden können. Wenn Sie DHTML zum Implementieren Ihres Handlers verwenden, muss er statisch sein. Um einen statischen Erweiterungshandler zu registrieren, erstellen Sie unter dem Unterschlüssel **Static** des Unterschlüssels **FindExtensions** einen Unterschlüssel namens für den Handler. Der Name wird vom System nicht verwendet, darf aber nicht mit anderen Suchhandlernamen unter dem Unterschlüssel **FindExtensions** identisch sein.

### <a name="shortcut-menu-based-search-handlers"></a>Kontextmenübasierte Suchhandler

Wenn Ihr Handler als [Kontextmenühandler](/windows/desktop/shell/context-menu-handlers)implementiert ist, legen Sie den Standardwert des Namensunterschlüssels des Handlers auf die CLSID-GUID (Class Identifier) des Objekts fest. Erstellen Sie unter dem Unterschlüssel name des Handlers einen Unterschlüssel mit dem Namen **0** (null), und legen Sie seinen Standardwert auf die Zeichenfolge fest, die im Untermenü **Suchen** oder **Suchen** angezeigt wird. Sie können Tastenkombinationen auf die übliche Weise aktivieren, indem Sie dem Tastenkombinationszeichen ein ampersand (&) vorangehen. Sie können ein optionales kleines Symbol rechts neben dem Menütext anzeigen lassen, indem Sie unter dem Unterschlüssel **0** einen **DefaultIcon-Unterschlüssel** erstellen. Legen Sie den Standardwert auf eine Zeichenfolge fest, die den Pfad der Datei enthält, die das Symbol enthält, gefolgt von einem Komma und dem nullbasierten Index des Symbols.

Im folgenden Beispiel wird der **Suchhandler MySearchEngine** registriert. Der Menütext lautet "Meine Suchmaschine", wobei M als Tastenkombination angegeben ist. Das Symbol befindet sich in C: \\ MyDir \\MySearch.dll mit einem Index von 2.

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

### <a name="dhtml-based-search-handlers"></a>DHTML-basierte Suchhandler

Mit Windows 2000 können Sie auch einen Suchhandler als DHTML-Dokument implementieren. Der Name wird im Untermenü **Suchen** des **Startmenüs** aufgeführt. Wenn der Benutzer ihn auswählt, wird Windows Explorer gestartet, wobei die Explorer-Leiste für das Suchdokument geöffnet wird. Sie können auch ein DHTML-Dokument angeben, das rechts neben der Explorer-Leiste angezeigt werden soll. Es gibt keine Möglichkeit, einen anderen Handler aus dem Standardmäßigen Suchbereich zu starten. Suchmaschinen können direkt über Windows Explorer gestartet werden, jedoch nur, wenn sie als [Bandobjekte](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85))implementiert sind.

Legen Sie zum Registrieren eines DHTML-basierten Suchhandlers den Namensunterschlüssel des Handlers auf die Zeichenfolgenform CLSID \_ ShellSearchExt (derzeit {169A0691-8DF9-11d1-A1C4-00C04FD75D13}) fest, und erstellen Sie die folgenden Unterschlüssel.

1.  Erstellen Sie unter dem Unterschlüssel handlername einen Unterschlüssel **0**(null), und legen Sie dessen Standardwert auf den Menütext fest.
2.  Damit neben dem Menütext ein Symbol angezeigt wird, erstellen Sie unter **0** einen **DefaultIcon-Unterschlüssel,** und legen Sie dessen Standardwert auf den Pfad und index des Symbols fest.
3.  Erstellen Sie unter **0** einen **SearchGUID-Unterschlüssel.** Weisen Sie dem DHTML-Dokument eine GUID zu, und legen Sie den Standardwert von **SearchGUID** auf das Zeichenfolgenformat fest. Diese GUID muss nicht unter **HKEY \_ CLASSES ROOT \_ \\ CLSID** registriert werden.
4.  Erstellen Sie unter **SearchGUID** einen URL-Unterschlüssel.  Legen Sie den Standardwert auf den Pfad des HTML-Dokuments fest, das in der Explorer-Leiste angezeigt wird.
5.  Erstellen Sie unter **SearchGUID** einen **UrlNavNew-Unterschlüssel.** Legen Sie den Standardwert auf den Pfad des HTML-Dokuments fest, das rechts neben der Explorer-Leiste angezeigt wird.

Im folgenden Beispiel wird der **Suchhandler MySearchEngine** registriert, der als DHTML-Dokument implementiert ist. Der Menütext lautet "Meine Suchmaschine", wobei M als Tastenkombination angegeben ist. Das Symbol befindet sich in C: \\ MyDir \\MySearch.dll mit einem Index von 2. Das DHTML-Dokument der Explorer-Leiste ist C: \\ MyDir \\MySearch.htm, und das Dokument, das rechts neben der Explorer-Leiste angezeigt wird, ist C: \\ MyDir \\MySearchPage.htm.

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

### <a name="registering-a-dynamic-search-handler"></a>Registrieren eines dynamischen Suchhandlers

Wenn Ihr Handler als [Kontextmenühandler](/windows/desktop/shell/context-menu-handlers)implementiert ist, können Sie ihn auch als dynamischen Handler registrieren. In diesem Fall wird sie mit der Shell geladen und nur beendet, wenn die Shell beendet wird. Dynamische Suchhandler reagieren viel schneller als statische Handler, wenn sie vom Benutzer gestartet werden. Dieser Ansatz funktioniert am besten, wenn das Laden der DLL Ihres Handlers lange dauern kann oder wenn sie wahrscheinlich häufig aufgerufen wird.

Dynamische Suchhandler werden unter dem Unterschlüssel **FindExtensions** registriert.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

Erstellen Sie einen Unterschlüssel von **FindExtensions** mit dem Namen für den Handler, und legen Sie dessen Standardwert auf die CLSID-GUID des Handlers fest. Menüsymbole werden für dynamische Suchhandler nicht unterstützt. Im folgenden Beispiel wird MySearchEngine als dynamischer Suchhandler registriert.

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

Im Gegensatz zu statischen Suchhandlern geben Sie den Menütext nicht in der Registrierung an. Wenn der Handler geladen wird, ruft die Shell die [**IContextMenu::QueryContextMenu-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) des Handlers auf, um elemente zum Untermenü **Suchen** oder **Suchen** hinzuzufügen.

## <a name="implementing-search-handlers"></a>Implementieren von Suchhandlern

Suchhandler können als Kontextmenühandler für alle Versionen von Windows implementiert werden. Für Windows 2000 können sie auch als DHTML-Dokumente implementiert werden.

Eine allgemeine Erläuterung der Implementierung von Kontextmenühandlern finden Sie unter [Erstellen von Kontextmenühandlern.](/windows/desktop/shell/context-menu-handlers) Suchhandler unterscheiden sich nur auf wenige Arten von standardverknüpfungsmenühandlern.

Für statische Menühandler wird das Untermenü **Suchen** oder **Suchen** aus den Informationen in der Registrierung erstellt. Es ist nicht erforderlich, dass der Handler ein Menüelement hinzufüge, wie es ein normaler Kontextmenühandler wäre. Die Shell verwaltet statische Menühandler wie folgt.

-   Wenn der Benutzer das Menüelement des Handlers startet, lädt die Shell die DLL des Handlers und ruft [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) auf, um den Handler zum Starten der Suchmaschine zu benachrichtigen. Die [**Methoden IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) und [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) werden nicht aufgerufen.
-   Wenn [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) aufgerufen wird, identifiziert der **lpVerb-Member** der [**übergebenen CMINVOKECOMMANDINFO-Struktur**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) den Befehl. Das Wort **lpVerb** in niedriger Reihenfolge wird auf die numerische Entsprechung des Unterschlüsselnamens des Befehls festgelegt. Da dieser Unterschlüssel normalerweise den Namen **0** hat, wird **lpVerb** in der Regel auf 0 (null) festgelegt. Der Handler sollte dann die Suchmaschine starten.

Dynamische Suchhandler werden ähnlich wie normale Kontextmenühandler implementiert. Die primäre Ausnahme besteht darin, dass beim Aufruf von [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) die Argumente *pidlFolder* und *lpdobj* auf **NULL** festgelegt werden.

DHTML-basierte Suchhandler werden als normales DHTML-Dokument implementiert. Sie können jede HTML-, DHTML- oder Skripttechnologie enthalten, die von Windows Internet Explorer unterstützt wird.

 

 