---
title: Erstellen einer Menübandanwendung
description: Das Windows Menüband-Framework besteht aus zwei unterschiedlichen, aber abhängigen Entwicklungsplattformen, einer Markupsprache, die auf Extensible Application Markup Language (XAML) zum Deklarieren von Steuerelementen und deren visuellem Layout basiert, und einem C++-Component Object Model (COM)-basierten Satz von Schnittstellen zum Definieren von Befehlsfunktionen und Anwendungshooks. Diese Arbeitsaufteilung innerhalb der Menüband-Frameworkarchitektur erfordert, dass ein Entwickler, der die umfassenden Benutzeroberflächenfunktionen des Frameworks nutzen möchte, die Benutzeroberfläche im Markup entwerfen und beschreiben und dann die COM-Schnittstellen des Menübandframeworks verwenden muss, um das Framework mit der Hostanwendung zu verbinden.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Windows Menüband, Erstellen von Anwendungen
- Menüband, Erstellen von Anwendungen
- Windows Menüband, Roadmap
- Menüband, Roadmap
- Windows Menüband, Markup
- Menüband, Markup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3cc3395b2fe53759152f5d0244c6546c08832bda190035a918af6049a99811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850029"
---
# <a name="creating-a-ribbon-application"></a>Erstellen einer Menübandanwendung

Das Windows Menübandframework besteht aus zwei unterschiedlichen, aber abhängigen Entwicklungsplattformen: einer Markupsprache, die auf Extensible Application Markup Language (XAML) zum Deklarieren von Steuerelementen und deren visuellem Layout basiert, und einem C++-Component Object Model (COM)-basierten Satz von Schnittstellen zum Definieren von Befehlsfunktionen und Anwendungshooks. Diese Arbeitsaufteilung innerhalb der Menüband-Frameworkarchitektur erfordert, dass ein Entwickler, der die umfassenden Benutzeroberflächenfunktionen des Frameworks nutzen möchte, die Benutzeroberfläche im Markup entwerfen und beschreiben und dann die COM-Schnittstellen des Menübandframeworks verwenden muss, um das Framework mit der Hostanwendung zu verbinden.

-   [Roadmap für Menüband](#ribbon-roadmap)
-   [Schreiben des Markups](#write-the-markup)
    -   [Kompilieren des Markups](#compile-the-markup)
-   [Erstellen der Anwendung](#build-the-application)
    -   [Initialisieren des Menübands](#initialize-the-ribbon)
    -   [Verknüpfen des Markups mit der Anwendung](#link-the-markup-to-the-application)
    -   [Kompilieren der Anwendung](#link-the-markup-to-the-application)
-   [Laufzeitupdates und -ausführungen](#run-time-updates-and-executions)
-   [OLE-Unterstützung](#ole-support)
-   [Zugehörige Themen](#related-topics)

## <a name="ribbon-roadmap"></a>Roadmap für Menüband

Die visuellen Aspekte einer Menübandanwendung, z. B. welche Steuerelemente angezeigt werden und wo sie platziert werden, werden im Markup deklariert (siehe [Deklarieren von Befehlen und Steuerelementen mit Menübandmarkup](windowsribbon-schema.md)). Die Logik des Anwendungsbefehls, z. B. was geschieht, wenn eine Schaltfläche gedrückt wird, wird im Code implementiert.

Der Prozess der Implementierung eines Menübands und derEntbindung in eine Windows Anwendung erfordert vier grundlegende Aufgaben: Schreiben des Markups, Kompilieren des Markups, Schreiben des Codes und Kompilieren und Verknüpfen der gesamten Anwendung.

Das folgende Diagramm veranschaulicht den Workflow für eine typische Menübandimplementierung.

![Diagramm, das den Workflow für eine typische Menübandimplementierungen zeigt.](images/overviews/ribbonroadmap.png)

In den folgenden Abschnitten wird dieser Prozess ausführlicher beschrieben.

## <a name="write-the-markup"></a>Schreiben des Markups

Nachdem die Menüband-Benutzeroberfläche entworfen wurde, besteht die erste Aufgabe für einen Anwendungsentwickler darin, die Benutzeroberfläche mit Menübandmarkup zu beschreiben.

> [!IMPORTANT]
> Die Menübandframework-Markupschemadatei UICC.xsd wird mit dem Microsoft Windows Software Development Kit (SDK) für Windows 7 und .NET Framework 4.0 installiert. Unter Verwendung des Standardinstallationspfads befindet sich die Datei im Ordner %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ Versionsnummer \] \\ Bin, in dem viele XML-Editoren auf sie verweisen können, um Hinweise und automatische Vervollständigung bereitzustellen.

 

Menübandsteuerelemente, Menübandbefehle (die steuerelementunabhängigen Elemente, die die Basisfunktionalität für Menübandsteuerelemente bereitstellen) und alle Steuerelementlayout- und visuellen Beziehungen werden im Markup deklariert. Die Struktur des Menübandmarkups hebt den Unterschied zwischen Menübandsteuerelementen und Befehlen durch zwei primäre Knotenhierarchien hervor: eine [Commands- und Resources-Struktur und](windowsribbon-reference-elements-command.md) eine [Views-Struktur.](windowsribbon-reference-elements-view.md)

Alle Container und Aktionen, die vom Menüband verfügbar gemacht werden, werden in der [Struktur Befehle und Ressourcen](windowsribbon-reference-elements-command.md) deklariert. Jedes Command-Element ist einem Satz von Ressourcen zugeordnet, wie dies für den Benutzeroberflächenentwurf erforderlich ist.

Nachdem Sie die Befehle für eine Anwendung erstellt haben, deklarieren Sie Steuerelemente in der [Ansichtsstruktur](windowsribbon-reference-elements-view.md) und binden jedes Steuerelement an einen Befehl, um die Befehlsfunktion verfügbar zu machen. Das Menübandframework bestimmt die tatsächliche Positionierung der Steuerelemente basierend auf der hier deklarierten Steuerelementhierarchie.

Im folgenden Codebeispiel wird veranschaulicht, wie Sie ein Button-Steuerelement mit der Bezeichnung Exit-Anwendung deklarieren und einem Exitbefehl zuordnen.


```
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
  <Application.Commands>
    <Command Name="cmdExit" LabelTitle="Exit application" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.Tabs>
        <Tab>
          <Group>
            <Button CommandName="cmdExit" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>
</Application>
        
```



> [!TIP]
> Es ist zwar möglich, eine beliebige Dateinamenerweiterung für die Menüband-Markupdatei zu verwenden, aber .xml ist die empfohlene Erweiterung, die in der gesamten Dokumentation verwendet wird.

 

### <a name="compile-the-markup"></a>Kompilieren des Markups

Nachdem die Menüband-Markupdatei erstellt wurde, muss sie vom Menübandmarkupcompiler UI Command Compiler (UICC), der im Windows Software Development Kit (SDK) enthalten ist, in ein Binärformat kompiliert werden. Ein Verweis auf diese Binärdatei wird während der Initialisierung des Menübandframeworks durch die Hostanwendung an die [**IUIFramework::LoadUI-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) übergeben.

UICC kann direkt über ein Befehlszeilenfenster ausgeführt oder als "Benutzerdefinierter Buildschritt" in Visual Studio hinzugefügt werden.

Die folgende Abbildung zeigt den UICC-Markupcompiler im CMD Shell-Fenster Windows 7 SDK.

![Screenshot, der uicc.exe in einem Befehlszeilenfenster zeigt.](images/overviews/screenshot-intentcl-commandline.png)

Die folgende Abbildung zeigt UICC, das in Visual Studio als benutzerdefinierter Buildschritt hinzugefügt wurde.

![Screenshot, der zeigt, uicc.exe als benutzerdefinierter Buildschritt in Visual Studio hinzugefügt wurde.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

Die UICC generiert drei Dateien: eine binäre Version des Markups (.bml), einen ID-Definitionsheader (H-Datei), um Markupelemente für die Menübandhostanwendung verfügbar zu machen, und ein [Ressourcendefinitionsskript (RC-Datei),](../menurc/about-resource-files.md) um Menübandimage- und Zeichenfolgenressourcen zur Kompilierzeit mit der Hostanwendung zu verknüpfen.

Weitere Informationen zum Kompilieren von Menübandframework-Markup finden Sie unter [Kompilieren von Menübandmarkup](windowsribbon-intentcl.md).

## <a name="build-the-application"></a>Erstellen der Anwendung

Nachdem die vorläufige Benutzeroberfläche für eine Menübandanwendung im Markup entworfen und implementiert wurde, muss Anwendungscode geschrieben werden, der das Framework initialisiert, das Markup nutzt und die im Markup deklarierten Befehle an die entsprechenden Befehlshandler in der Anwendung bindet.

> [!IMPORTANT]
>
> Da das Menübandframework COM-basiert ist, wird empfohlen, dass Menübandprojekte den \_ \_ Operator uuidof() verwenden, um auf die GUIDs für Menübandframeworkschnittstellen (IIDs) zu verweisen. In Fällen, in denen es nicht möglich ist, den \_ \_ uuidof()-Operator zu verwenden, z. B. wenn ein Nicht-Microsoft-Compiler verwendet wird oder die Hostanwendung C-basiert ist, müssen die IIDs von der Anwendung definiert werden, da sie nicht in uuid.lib enthalten sind.
>
> Wenn die IIDs von der Anwendung definiert werden, müssen die in UIRibbon.idl angegebenen GUIDs verwendet werden.
>
> UIRibbon.idl ist teil des [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) und befindet sich im Standardinstallationspfad von %ProgramFiles% Microsoft \\ SDKs Windows \\ \\ v7.0 \\ Include.

 

### <a name="initialize-the-ribbon"></a>Initialisieren des Menübands

Das folgende Diagramm veranschaulicht die Schritte, die zum Implementieren einer einfachen Menübandanwendung erforderlich sind.

![Diagramm, das die Schritte zeigt, die zum Implementieren einer einfachen Menübandimplementierungen erforderlich sind.](images/overviews/initializationsteps.png)

In den folgenden Schritten wird ausführlich beschrieben, wie Sie eine einfache Menübandanwendung implementieren.

1.  Cocreateinstance

    Die Anwendung ruft die COM CoCreateInstance-Standardfunktion mit der Klassen-ID des Menübandframeworks auf, um einen Zeiger auf das Framework abzurufen.

    ```
    IUIFramework* pFramework = NULL;
    HRESULT hr = ::CoCreateInstance(
                CLSID_UIRibbonFramework, 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pFramework));
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

2.  Initialize(hwnd, IUIApplication \* )

    Die Anwendung ruft [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize)auf und übergibt zwei Parameter: das Handle für das Fenster der obersten Ebene, das das Menüband enthält, und einen Zeiger auf die [**IUIApplication-Implementierung,**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) die es dem Framework ermöglicht, Rückrufe für die Anwendung durchzuführen.

    > \[! Wichtig\]  
    > Das Menübandframework wird als Singlethread-Apartment (STA) initialisiert.

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  LoadUI(instanz, resourceName)

    Die Anwendung ruft [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) auf, um die Markupressource zu binden. Der erste Parameter dieser Funktion ist ein Handle für die Menübandanwendungsinstanz. Der zweite Parameter ist der Name der binären Markupressource, die zuvor kompiliert wurde. Indem das binäre Markup an das Menübandframework übergeben wird, signalisiert die Anwendung, wie die Menübandstruktur aussehen soll und wie Steuerelemente angeordnet werden sollen. Außerdem wird dem Framework ein Manifest von Befehlen zur Verfügung gestellt (z. B. Einfügen, Ausschneiden, Suchen), die vom Framework verwendet werden, wenn befehlsbezogene Rückrufe zur Laufzeit ausgeführt werden.

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  [**IUIApplication::OnCreateUICommand-Rückrufe**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)

    Nach Abschluss der Schritte 1 bis 3 weiß das Menübandframework, welche Befehle im Menüband verfügbar gemacht werden sollen. Das Framework benötigt jedoch noch zwei Dinge, bevor das Menüband voll funktionsfähig ist: eine Möglichkeit, der Anwendung mitzuteilen, wann Befehle ausgeführt werden, und eine Möglichkeit zum Abrufen von Befehlsressourcen oder Eigenschaften zur Laufzeit. Wenn beispielsweise ein Kombinationsfeld auf der Benutzeroberfläche angezeigt werden soll, muss das Framework nach den Elementen fragen, mit denen das Kombinationsfeld aufgefüllt werden soll.

    Diese beiden Funktionen werden über die [**IUICommandHandler-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) verarbeitet. Insbesondere ruft das Framework für jeden im binären Markup deklarierten Befehl (siehe Schritt 3 [**oben) IUIApplication::OnCreateUICommand auf,**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) um die Anwendung nach einem **IUICommandHandler-Objekt** für diesen Befehl zu fragen.

    > [!Note]  
    > Mit der [**IUICommandHandler-Schnittstelle**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) kann ein Befehlshandler an einen oder mehrere Befehle gebunden werden.

     

Die Anwendung muss mindestens Stubs mit [**IUIApplication-Methoden**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) implementieren, die E NOTIMPL zurückgeben, \_ wie im folgenden Beispiel gezeigt.


```
STDMETHOD(OnViewChanged)(UINT32 viewId,
                         UI_VIEWTYPE typeID,
                         IUnknown *view,
                         UI_VIEWVERB verb,
                         INT32 uReasonCode)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnCreateUICommand)(UINT32 commandId,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler **commandHandler)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnDestroyUICommand)(UINT32 commandId,
                              UI_COMMANDTYPE typeID,
                              IUICommandHandler *commandHandler) 
{ 
  return E_NOTIMPL; 
}
```



### <a name="link-the-markup-to-the-application"></a>Verknüpfen des Markups mit der Anwendung

An diesem Punkt müssen die Markupressourcendateien mit der Hostanwendung verknüpft werden, indem ein Verweis auf die Markupressourcendefinitionsdatei (die einen Verweis auf die Markupheaderdatei enthält) in die Ressourcendatei der Anwendung eingeschlossen wird. Beispielsweise erfordert eine Anwendung namens RibbonApp mit einer Ressourcendatei namens ribbonUI.rc die folgende Zeile in der Datei RibbonApp.rc.


```C++
#include "ribbonUI.rc"
```



Abhängig vom verwendeten Compiler und Linker erfordert das Ressourcendefinitionsskript möglicherweise auch eine Kompilierung, bevor die Menübandanwendung kompiliert werden kann. Das Befehlszeilentool [ressourcencompiler (RC),](../menurc/using-rc-the-rc-command-line-.md) das mit Microsoft Visual Studio und dem Windows SDK ausgeliefert wird, kann für diese Aufgabe verwendet werden.

### <a name="compile-the-application"></a>Kompilieren der Anwendung

Nachdem die Menübandanwendung kompiliert wurde, kann sie ausgeführt und die Benutzeroberfläche getestet werden. Wenn die Benutzeroberfläche optimiert werden muss und keine Änderungen an zugeordneten Befehlshandlern im Hauptanwendungscode vorgenommen werden, überarbeiten Sie die Markupquelldatei, kompilieren Sie das Markup mit UICC.exe neu, und verknüpfen Sie die neuen Markupressourcendateien. Wenn die Anwendung neu gestartet wird, wird die geänderte Benutzeroberfläche angezeigt.

All dies ist möglich, ohne den Kernanwendungscode zu berühren – eine erhebliche Verbesserung gegenüber der Entwicklung und Verteilung von Standardanwendungen.

## <a name="run-time-updates-and-executions"></a>Laufzeitupdates und -ausführungen

Die Laufzeitkommunikationsstruktur des Menübandframeworks basiert auf einem Push- und Pullmodell oder einem zweiseitigen Aufrufermodell.

Dieses Modell ermöglicht es dem Framework, die Anwendung zu informieren, wenn ein Befehl ausgeführt wird, und ermöglicht es sowohl dem Framework als auch der Anwendung, Eigenschaftswerte und Menübandressourcen abzufragen, zu aktualisieren und für ungültig zu erklären. Diese Funktionalität wird über eine Reihe von Schnittstellen und Methoden bereitgestellt.

Das Framework ruft aktualisierte Eigenschafteninformationen aus der Menübandanwendung über die [**Rückrufmethode IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) ab. Eine Befehls-ID und ein Eigenschaftenschlüssel, der die zu aktualisierende Command-Eigenschaft identifiziert, werden an die Methode übergeben, die dann einen Wert für diesen Eigenschaftsschlüssel an das Framework zurückgibt oder pusht.

Das Framework ruft [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) auf, wenn ein Befehl ausgeführt wird. Dabei werden sowohl die Befehls-ID als auch der Typ der aufgetretenen Ausführung identifiziert ([**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)). Hier gibt die Anwendung die Ausführungslogik für einen Befehl an.

Das folgende Diagramm veranschaulicht die Laufzeitkommunikation für die Befehlsausführung zwischen dem Framework und der Anwendung.

![Diagramm, das ein Beispiel für die Laufzeitkommunikation zwischen dem Menübandframework und einer Hostanwendung zeigt.](images/overviews/updatesandexecutions.png)

> [!Note]  
> Die Implementierung [**der Funktionen IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) und [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) ist nicht erforderlich, um zunächst ein Menüband in einer Anwendung anzuzeigen. Diese Methoden sind jedoch erforderlich, um sicherzustellen, dass die Anwendung ordnungsgemäß funktioniert, wenn Befehle vom Benutzer ausgeführt werden.

 

## <a name="ole-support"></a>OLE-Unterstützung

Eine Menübandanwendung kann als OLE-Server konfiguriert werden, um die out-of-place-OLE-Aktivierung zu unterstützen.

Objekte, die in einer OLE-Serveranwendung erstellt werden, behalten ihre Zuordnung zur Serveranwendung bei, wenn sie in eine OLE-Clientanwendung (oder einen -Container) eingefügt (eingefügt oder platziert) werden. Bei der nicht richtigen OLE-Aktivierung wird durch Doppelklicken auf das Objekt in der Clientanwendung eine dedizierte Instanz der Serveranwendung geöffnet und das Objekt zur Bearbeitung geladen. Wenn die Serveranwendung geschlossen wird, werden alle am Objekt vorgenommenen Änderungen in der Clientanwendung widergespiegelt.

> [!Note]  
> Das Menübandframework unterstützt keine inaktive OLE-Aktivierung. Objekte, die auf einem menübandbasierten OLE-Server erstellt wurden, können nicht innerhalb der OLE-Clientanwendung bearbeitet werden. Eine externe dedizierte Instanz der Serveranwendung ist erforderlich.


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deklarieren von Befehlen und Steuerelementen mit Menübandmarkup](./windowsribbon-schema.md)
</dt> <dt>

[Richtlinien für die Benutzerfreundlichkeit des Menübands](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Menübandentwurfsprozess](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




