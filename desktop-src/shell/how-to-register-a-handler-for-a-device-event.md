---
description: Beschreibt die Prozesse zum Implementieren von Geräteereignishandlern in der Registrierung.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Registrieren eines Handlers für ein Geräteereignis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a13abe8917d93ac6a4801e0c11cb7223da25e362923df229180b8c8e6211ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859599"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a>Registrieren eines Handlers für ein Geräteereignis

Handler definieren den Softwareteil der automatischen Wiedergabe. Sie definieren das Symbol und den Anzeigenamen der Software sowie die COM-Komponente (Component Object Model), die instanziiert werden soll und wie die Komponente als Reaktion auf ein Ereignis initialisiert wird. Jeder Handler für ein bestimmtes Ereignis wird als Wert unter dem entsprechenden **EventHandler-Schlüssel** registriert. Wenn dieses Ereignis erkannt wird, wird der Benutzer aufgefordert, einen Handler aus einer Liste aller Handler auszuwählen, die für dieses Ereignis registriert sind.

## <a name="instructions"></a>Anweisungen


Handler und ihre zugeordneten Werte werden unter dem **Schlüssel AutoplayHandlers** \\ **Handlers** definiert. Unterschlüssel unterscheiden sich abhängig davon, ob das System Geräteinhalte direkt lesen kann oder ob das Gerät Inhalte über eine proprietäre Schnittstelle für das System bereitstellt.

Das folgende Beispiel zeigt die Unterschlüssel und Werte, die für ein Gerät verwendet werden, z. B. eine digitale Videokamera oder .mp3 Player, die den Inhalt über eine proprietäre Schnittstelle für das System bereitstellt. Der Beispielhandler heißt **MyHandler.**

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
> Während das Beispiel sowohl einen ProgID- als auch einen CLSID-Wert (Class Identifier) zeigt, schließen sich diese Werte in der Praxis gegenseitig aus, sodass nur der eine oder der andere vorhanden ist. Der ProgID-Wert wird bevorzugt. Je nachdem, was verwendet wird, sollte es auf eine COM-Komponente verweisen, die die [**IHWEventHandler-Schnittstelle**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) implementiert.

 

Sie können den Aktionswert als Literalwert eingeben, z. B. "Musik wiedergeben", wie in diesem Beispiel gezeigt, oder als Dateiname mit einer Ressourcenzeichenfolge. Sie können den Anbieterwert auch als Literalwert oder als Dateinamen mit einer Ressourcenzeichenfolge eingeben. Bei der automatischen Wiedergabe werden der Aktionswert und der Anbieterwert mit dem Wort "using" kombiniert, um eine benutzerfreundliche Beschriftung zu erstellen, die auf der Benutzeroberfläche angezeigt wird. Im Beispiel lautet die resultierende Beschriftung "Musik mit Windows Media Player wiedergeben".

Der DefaultIcon-Wert verweist entweder auf eine ICO-Datei oder eine Ressource in einer Binärdatei. Wenn der numerische Wert, der dem Binärdateinamen folgt, 0 (null) oder größer ist, ist er der Indexwert des Symbols in dieser Binärdatei. Wenn es sich um einen negativen Wert handelt, handelt es sich um die Symbolressourcen-ID. Negative Indexwerte werden empfohlen. Bei einer ICO-Datei ist kein Wert erforderlich. Es wird empfohlen, umgebungsvariablen im Pfad zu verwenden.

Der InitCmdLine-Wert wird unverändert durch die [**IHWEventHandler::Initialize-Methode**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) übergeben, bevor andere Methoden aufgerufen werden.

Das folgende Beispiel zeigt die Unterschlüssel und Werte, die für ein Gerät verwendet werden, das direkt gelesen werden kann, z. B. ein CD-ROM-Laufwerk oder ein anderer Wechseldatenträger. Auch hier heißt der Beispielhandler **MyHandler**.

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

In diesem Beispiel werden die Werte Für Aktion und Anbieter als Dateiname mit einer Ressourcenzeichenfolge anstelle von Literalwerten angezeigt, aber die Zeichenfolgen, auf die sie verweisen, werden auf die gleiche Weise verwendet. Sie werden mit dem Wort "using" kombiniert, um eine benutzerfreundliche Beschriftung zu bilden, wie weiter oben erläutert.

InvokeProgID- und InvokeVerb-Werte ersetzen CLSID, InitCmdLine und ProgID. Die InvokeProgID- und InvokeVerb-Werte stimmen mit Schlüsselnamen überein, die sich unter **HKEY \_ CLASSES \_ ROOT** befinden, wie im folgenden Registrierungseintrag gezeigt. Dieser Satz von Beispielschlüsseln entspricht dem zuvor beschriebenen spezifischen Handlerbeispiel.

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

Die [**CoCreateInstance-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) verwendet die CLSID, um die entsprechende Anwendung zu implementieren.

Nachdem Sie den Handler auf eine dieser beiden Arten definiert haben, müssen Sie ihn für ein bestimmtes Ereignis registrieren. Dazu geben Sie den Handlernamen als Wert für den Schlüssel dieses Ereignisses unter **EventHandlers an.** Im folgenden Beispiel wird gezeigt, wie **MyHandler** als Handler für das GenericVolume Handler-Ereignis registriert wird. Ihm ist kein Datenwert zugewiesen.

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

[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
