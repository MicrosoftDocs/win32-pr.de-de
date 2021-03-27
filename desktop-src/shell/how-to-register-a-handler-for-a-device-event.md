---
description: Beschreibt die Prozesse für die Implementierung von Geräte Ereignis Handlern in der Registrierung.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Registrieren eines Handlers für ein Geräte Ereignis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef15071b349afa3f863e7c57b64c280c2aef8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864919"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a>Registrieren eines Handlers für ein Geräte Ereignis

Handler definieren den Software Teil von AutoPlay. Sie definieren das Symbol und den anzeigen amen der Software sowie die Komponente "Component Object Model (com)", die instanziiert werden soll, und wie die Komponente als Reaktion auf ein Ereignis initialisiert wird. Jeder Handler für ein bestimmtes Ereignis wird als Wert unter dem entsprechenden **EventHandler** -Schlüssel registriert. Wenn dieses Ereignis erkannt wird, wird der Benutzer aufgefordert, einen Handler aus einer Liste aller für dieses Ereignis registrierten Handler auszuwählen.

## <a name="instructions"></a>Instructions


Handler und die zugehörigen Werte werden unter dem Schlüssel " **autoplayhandlers** \\ **Handlers** " definiert. Unterschlüssel unterscheiden sich abhängig davon, ob das System den Geräte Inhalt direkt lesen kann oder ob das Gerät über eine proprietäre Oberfläche Inhalt für das System bereitstellt.

Das folgende Beispiel zeigt die Unterschlüssel und Werte, die für ein Gerät verwendet werden, z. b. eine digitale Videokamera oder MP3-Player, die den Inhalt des Systems über eine proprietäre Schnittstelle bereitstellt. Der Beispiel Handler heißt **MyHandler**.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = Play music
                           CLSID [REG_SZ] = {a51f2ed3-634e-4a97-9d55-efcf08e7b32f}
                           DefaultIcon [REG_EXPAND_SZ] = %ProgramFiles%\Windows Media Player\wmplayer.exe,0
                           InitCmdLine [REG_SZ] = /Play
                           ProgID [REG_SZ] = WMP.PlayMusicFiles
                           Provider [REG_SZ] = Windows Media Player
```

> [!Note]  
> Das Beispiel zeigt zwar sowohl einen ProgID-als auch einen Klassen Bezeichner (CLSID), aber in der Praxis schließen sich diese Werte gegenseitig aus, sodass nur eine oder die andere vorhanden ist. Der ProgID-Wert wird bevorzugt. Je nachdem, welche verwendet wird, sollte es auf eine COM-Komponente verweisen, die die [**ihweventhandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) -Schnittstelle implementiert.

 

Sie können den Aktionswert als Literalwert eingeben, z. b. "Musik abspielen", wie in diesem Beispiel gezeigt, oder als Dateiname mit einer Ressourcen Zeichenfolge. Sie können den Anbieter Wert auch als Literalwert oder als Dateinamen mit einer Ressourcen Zeichenfolge eingeben. AutoPlay kombiniert den Aktionswert und den Anbieter Wert mit dem Wort "using", um eine benutzerfreundliche Beschriftung zu erstellen, die auf der Benutzeroberfläche angezeigt wird. Im Beispiel ist die resultierende Beschriftung "Abspielen von Musik mit Windows Media Player".

Der DefaultIcon-Wert verweist entweder auf eine ICO-Datei oder auf eine Ressource in einer Binärdatei. Wenn der numerische Wert, der auf den Binär Dateinamen folgt, 0 (null) oder größer ist, dann ist dies der Indexwert des Symbols in dieser Binärdatei. Wenn es sich um einen negativen Wert handelt, ist dies die Symbol Ressourcen-ID. Es werden negative Indexwerte empfohlen. Im Fall einer ICO-Datei ist kein Wert erforderlich. Es wird empfohlen, Umgebungsvariablen im Pfad zu verwenden.

Der initcmdline-Wert übergibt unverändert durch die [**ihweventhandler:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) -Methode, bevor andere Methoden aufgerufen werden.

Das folgende Beispiel zeigt die Unterschlüssel und Werte, die für ein Gerät verwendet werden, das direkt gelesen werden kann, z. b. ein CD-ROM-Laufwerk oder einen anderen Wechsel Datenträger. Der Beispiel Handler wird auch als **MyHandler** bezeichnet.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-276
                           DefaultIcon [REG_EXPAND_SZ] = %systemroot%\System32\wiaacmgr.exe,-2
                           InvokeProgID [REG_SZ] = WIA.AutoPlayDropHandler
                           InvokeVerb [REG_SZ] = open
                           Provider [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-101
```

In diesem Beispiel werden die Aktions-und Anbieter Werte als Dateiname mit einer Ressourcen Zeichenfolge anstelle von Literalwerten angezeigt, aber die Zeichen folgen, auf die Sie verweisen, werden auf die gleiche Weise verwendet. Sie werden mit dem Wort "using" kombiniert, um eine benutzerfreundliche Beschriftung zu bilden, wie bereits erläutert.

Die Werte invokeprogid und invokeverb ersetzen CLSID, initcmdline und ProgID. Die Werte invokeprogid und invokeverb entsprechen den Schlüsselnamen, die unter **HKEY \_ Classes \_ root** gefunden werden, wie im folgenden Registrierungs Eintrag gezeigt. Diese Gruppe von Beispiel Schlüsseln entspricht dem zuvor beschriebenen spezifischen handlerbeispiel.

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

Die [**cokreateingestance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion verwendet die CLSID, um die entsprechende Anwendung zu implementieren.

Nachdem Sie den Handler auf eine dieser beiden Arten definiert haben, müssen Sie ihn für ein bestimmtes Ereignis registrieren. Hierzu geben Sie den Handlernamen als Wert für den Schlüssel dieses Ereignisses unter **Eventhandlers** an. Im folgenden Beispiel wird gezeigt, wie **MyHandler** als Handler für das genericvolumearrival-Ereignis registriert wird. Es ist kein Datenwert zugewiesen.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        GenericVolumeArrival
                           MyHandler [REG_SZ]
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ihweventhandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
