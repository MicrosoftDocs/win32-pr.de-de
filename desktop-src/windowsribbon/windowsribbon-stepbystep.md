---
title: Erstellen einer Menü Bandanwendung
description: Das Windows-Menüband-Framework besteht aus zwei unterschiedlichen, aber abhängigen Entwicklungsplattformen, eine Markup Sprache, die auf Extensible Application Markup Language (XAML) basiert, um Steuerelemente und deren visuelles Layout zu deklarieren, sowie einen auf C++ Component Object Model (com) basierenden Satz von Schnittstellen zum Definieren von Befehls Funktionalität und anwendungshooks. Diese Arbeitsabteilung innerhalb der Multifunktionsleisten-Framework-Architektur erfordert, dass ein Entwickler, der die umfassenden Benutzeroberflächen Funktionen des Frameworks nutzen möchte, die Benutzeroberfläche im Markup entwerfen und beschreiben muss und dann die COM-Schnittstellen des Menüband-Frameworks verwenden, um das Framework mit der Host Anwendung zu verbinden.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Windows-Menüband, Erstellen von Anwendungen
- Multifunktionsleiste, Erstellen von Anwendungen
- Windows-Menüband, Roadmap
- Menüband, Roadmap
- Windows-Menüband, Markup
- Menüband, Markup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a10f683c7fbb07b9992e418a4c09dc9aecba280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390740"
---
# <a name="creating-a-ribbon-application"></a>Erstellen einer Menü Bandanwendung

Das Windows-Menüband-Framework besteht aus zwei unterschiedlichen, aber abhängigen Entwicklungsplattformen: einer Markup Sprache, die auf Extensible Application Markup Language (XAML) basiert, um Steuerelemente und deren visuelles Layout zu deklarieren, und einem auf C++ Component Object Model (com) basierenden Satz von Schnittstellen zum Definieren von Befehls Funktionalität und anwendungshooks. Diese Arbeitsabteilung innerhalb der Multifunktionsleisten-Framework-Architektur erfordert, dass ein Entwickler, der die umfassenden Benutzeroberflächen Funktionen des Frameworks nutzen möchte, die Benutzeroberfläche im Markup entwerfen und beschreiben muss und dann die COM-Schnittstellen des Menüband-Frameworks verwenden, um das Framework mit der Host Anwendung zu verbinden.

-   [Menüband-Roadmap](#ribbon-roadmap)
-   [Schreiben des Markups](#write-the-markup)
    -   [Markup kompilieren](#compile-the-markup)
-   [Erstellen der Anwendung](#build-the-application)
    -   [Initialisieren der Multifunktionsleiste](#initialize-the-ribbon)
    -   [Das Markup mit der Anwendung verknüpfen](#link-the-markup-to-the-application)
    -   [Kompilieren der Anwendung](#link-the-markup-to-the-application)
-   [Lauf Zeit Updates und Ausführungen](#run-time-updates-and-executions)
-   [OLE-Unterstützung](#ole-support)
-   [Zugehörige Themen](#related-topics)

## <a name="ribbon-roadmap"></a>Menüband-Roadmap

Die visuellen Aspekte einer Menü Bandanwendung, wie z. b. welche Steuerelemente angezeigt werden und wo Sie platziert werden, werden im Markup deklariert (siehe [Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup](windowsribbon-schema.md)). Die Anwendungs Befehls Logik, z. b. Was geschieht, wenn eine Schaltfläche gedrückt wird, wird im Code implementiert.

Der Prozess der Implementierung eines Menübands und der Einbindung in eine Windows-Anwendung erfordert vier grundlegende Aufgaben: Schreiben Sie das Markup, kompilieren Sie das Markup, schreiben Sie den Code, und kompilieren und verknüpfen Sie die gesamte Anwendung.

Das folgende Diagramm veranschaulicht den Workflow für eine typische multifunktionsleistenimplementierung.

![das Diagramm zeigt den Workflow für eine typische Multifunktionsleisten Implementierung.](images/overviews/ribbonroadmap.png)

In den folgenden Abschnitten wird dieser Prozess ausführlicher beschrieben.

## <a name="write-the-markup"></a>Schreiben des Markups

Nachdem die Multifunktionsleisten-Benutzeroberfläche entworfen wurde, besteht die erste Aufgabe für einen Anwendungsentwickler darin, die Benutzeroberfläche mit Menüband-Markup zu beschreiben.

> [!IMPORTANT]
> Die Markup Schema Datei uicc. xsd von Ribbon Framework wird mit dem Microsoft Windows Software Development Kit (SDK) für Windows 7 und .NET Framework 4,0 installiert. Wenn Sie den Standard Installationspfad verwenden, befindet sich die Datei im Ordner% Program Files% \\ Microsoft sdert \\ Windows \\ \[ Version Number bin, in \] \\ dem von vielen XML-Editoren auf Sie verwiesen werden kann, um Hinweise und automatische Vervollständigung bereitzustellen.

 

Menü Band Steuerelemente, Menü Band Befehle (die Steuerelement unabhängigen Elemente, die die Basisfunktionalität für Menüband-Steuerelemente bereitstellen), und das gesamte Steuerelement Layout und visuelle Beziehungen werden im Markup deklariert. Die Struktur des Menü Band Markups hebt den Unterschied zwischen Menüband-Steuerelementen und Befehlen durch zwei primäre Knoten Hierarchien hervor: eine Struktur von [Befehlen und Ressourcen](windowsribbon-reference-elements-command.md) [sowie eine](windowsribbon-reference-elements-view.md) Ansichts Struktur.

Alle Container und Aktionen, die über das Menüband verfügbar gemacht werden, werden in der Struktur " [Befehle und Ressourcen](windowsribbon-reference-elements-command.md) " deklariert. Jedes Command-Element ist einem Satz von Ressourcen zugeordnet, die vom Benutzeroberflächen Entwurf benötigt werden.

Nachdem Sie die Befehle für eine Anwendung erstellt haben, deklarieren Sie Steuerelemente in der Struktur [Sichten](windowsribbon-reference-elements-view.md) und binden jedes Steuerelement an einen Befehl, um die Befehls Funktionalität verfügbar zu machen. Das Menüband-Framework bestimmt die tatsächliche Positionierung der Steuerelemente auf der Grundlage der hier deklarierten Steuerelement Hierarchie.

Im folgenden Codebeispiel wird veranschaulicht, wie Sie ein Schaltflächen-Steuerelement mit der Bezeichnung Exit Application deklarieren und einem Exit-Befehl zuordnen.


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
> Obwohl es möglich ist, eine beliebige Dateinamenerweiterung für die Menüband-Markup Datei zu verwenden, ist XML die empfohlene Erweiterung, die in der gesamten Dokumentation verwendet wird.

 

### <a name="compile-the-markup"></a>Markup kompilieren

Nachdem die Menüband-Markup Datei erstellt wurde, muss Sie vom Menüband-Markup Compiler (UICC), der im Windows-Software Development Kit (SDK) enthalten ist, in ein binäres Format kompiliert werden. Ein Verweis auf diese Binärdatei wird während der Initialisierung des Menüband-Frameworks von der Host Anwendung an die [**iuiframework:: loadui**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) -Methode übermittelt.

UICC kann direkt über ein Befehlszeilenfenster ausgeführt oder als "benutzerdefinierter Buildschritt" in Visual Studio hinzugefügt werden.

In der folgenden Abbildung wird der UICC Markup Compiler im Windows 7 SDK-cmd-Shellfenster gezeigt.

![Screenshot, der uicc.exe in einem Befehlszeilenfenster anzeigt.](images/overviews/screenshot-intentcl-commandline.png)

Die folgende Abbildung zeigt UICC, das als benutzerdefinierter Buildschritt in Visual Studio hinzugefügt wurde.

![Screenshot, der zeigt, uicc.exe als benutzerdefinierter Buildschritt in Visual Studio hinzugefügt wurde.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

Das UICC generiert drei Dateien: eine binäre Version des Markups (. BML), einen ID-Definitions Header (h-Datei) zum verfügbar machen von Markup Elementen für die Menüband-Host Anwendung und ein [Ressourcen Definitions Skript](../menurc/about-resource-files.md) (RC-Datei), um das Menüband Bild und die Zeichen folgen Ressourcen zur Kompilierzeit mit der Host Anwendung zu verknüpfen.

Ausführlichere Informationen zum Kompilieren von Multifunktionsleisten-Frameworks finden Sie unter Kompilieren von Menü [Band Markup](windowsribbon-intentcl.md).

## <a name="build-the-application"></a>Erstellen der Anwendung

Nachdem die vorläufige Benutzeroberfläche für eine Multifunktionsleistenanwendung im Markup entworfen und implementiert wurde, muss der Anwendungscode geschrieben werden, der das Framework initialisiert, das Markup nutzt und die im Markup deklarierten Befehle an die entsprechenden Befehls Handler in der Anwendung bindet.

> [!IMPORTANT]
>
> Da das Multifunktionsleisten-Framework com-basiert ist, wird empfohlen, dass Menü Bandprojekte den \_ \_ uuidof ()-Operator verwenden, um auf die GUIDs für Menüband Framework-Schnittstellen (IIDs) zu verweisen. In Fällen, in denen es nicht möglich ist, den \_ \_ uuidof ()-Operator zu verwenden, z. b. Wenn ein nicht-Microsoft-Compiler verwendet oder die Host Anwendung C-basiert ist, müssen die IIDs von der Anwendung definiert werden, da Sie nicht in UUID. lib enthalten sind.
>
> Wenn die IIDs von der Anwendung definiert werden, müssen die in uiribbon. idl angegebenen GUIDs verwendet werden.
>
> Uiribbon. idl ist Teil des [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) und befindet sich im Standard Installationspfad von% Program Files% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ include.

 

### <a name="initialize-the-ribbon"></a>Initialisieren der Multifunktionsleiste

Das folgende Diagramm veranschaulicht die Schritte, die zum Implementieren einer einfachen Multifunktionsleistenanwendung erforderlich sind.

![Diagramm mit den Schritten, die zum Implementieren einer einfachen Multifunktionsleisten-Implementierung erforderlich sind.](images/overviews/initializationsteps.png)

In den folgenden Schritten wird ausführlich beschrieben, wie eine einfache Menü Bandanwendung implementiert wird.

1.  CoCreateInstance

    Die Anwendung ruft die com-Standard-cokreateinstance-Funktion mit der Multifunktionsleisten-Framework-Klassen-ID auf, um einen Zeiger auf das Framework abzurufen.

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

    

2.  Initialisieren (HWND, iuiapplication \* )

    Die Anwendung ruft [**iuiframework:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize)auf und übergibt zwei Parameter: das Handle für das Fenster auf oberster Ebene, das das Menüband enthält, und einen Zeiger auf die [**iuiapplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) -Implementierung, die es dem Framework ermöglicht, Rückrufe für die Anwendung zu erstellen.

    > \[! Wichtig\]  
    > Das Menüband-Framework wird als Single Thread-Apartment (STA) initialisiert.

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  Loadui (Instanz, resourceName)

    Die Anwendung ruft [**iuiframework:: loadui**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) auf, um die Markup Ressource zu binden. Der erste Parameter dieser Funktion ist ein Handle für die Menüband-Anwendungs Instanz. Der zweite Parameter ist der Name der zuvor kompilierten binären Markup Ressource. Indem das binäre Markup an das Multifunktionsleisten-Framework übergeben wird, signalisiert die Anwendung, wie die Menüband-Struktur lauten soll und wie Steuerelemente angeordnet werden sollten. Außerdem bietet das Framework ein Manifest von Befehlen, die verfügbar gemacht werden (z. b. einfügen, Ausschneiden, suchen), die vom Framework verwendet werden, wenn es Befehls bezogene Rückrufe zur Laufzeit ausführt.

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  [**Iuiapplication:: onkreateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) -Rückrufe

    Nachdem die Schritte 1 bis 3 abgeschlossen sind, weiß das Menüband-Framework, welche Befehle im Menüband verfügbar gemacht werden sollen. Das Framework benötigt jedoch noch zwei Dinge, bevor das Menüband voll funktionsfähig ist: eine Methode, um der Anwendung mitzuteilen, wann Befehle ausgeführt werden und wie Sie zur Laufzeit Befehls Ressourcen oder Eigenschaften erhalten. Wenn z. b. ein Kombinations Feld in der Benutzeroberfläche angezeigt werden soll, muss das Framework die Elemente Abfragen, mit denen das Kombinations Feld aufgefüllt werden soll.

    Diese beiden Funktionen werden über die [**iuicommandhandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) -Schnittstelle behandelt. Insbesondere für jeden Befehl, der im binären Markup deklariert ist (siehe Schritt 3 oben), ruft das Framework [**iuiapplication:: onforateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) auf, um die Anwendung nach einem **iuicommandhandler** -Objekt für diesen Befehl zu Fragen.

    > [!Note]  
    > Mit der [**iuicommandhandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) -Schnittstelle kann ein Befehls Handler an einen oder mehrere Befehle gebunden werden.

     

Die Anwendung muss mindestens [**iuiapplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) Methodenstub implementieren, die E \_ notimpl zurückgeben, wie im folgenden Beispiel gezeigt.


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



### <a name="link-the-markup-to-the-application"></a>Das Markup mit der Anwendung verknüpfen

An diesem Punkt müssen die Markup Ressourcen Dateien mit der Host Anwendung verknüpft werden, indem ein Verweis auf die Markup Ressourcen Definitionsdatei (die einen Verweis auf die Markup Header Datei enthält) in der Anwendungs Ressourcen Datei eingeschlossen wird. Beispielsweise ist für eine Anwendung mit dem Namen "ribbonapp" mit der Ressourcen Datei "ribbonui. RC" die folgende Zeile in der Datei "ribbonapp. RC" erforderlich.


```C++
#include "ribbonUI.rc"
```



Abhängig vom verwendeten Compiler und Linker kann das Ressourcen Definitions Skript auch kompiliert werden, bevor die Multifunktionsleistenanwendung kompiliert werden kann. Das Befehlszeilen Tool des [Ressourcen Compilers (RC)](../menurc/using-rc-the-rc-command-line-.md) , das im Lieferumfang von Microsoft Visual Studio und der Windows SDK enthalten ist, kann für diese Aufgabe verwendet werden.

### <a name="compile-the-application"></a>Kompilieren der Anwendung

Nachdem die Menüband-Anwendung kompiliert wurde, kann Sie ausgeführt und die Benutzeroberfläche getestet werden. Wenn die Benutzeroberfläche optimiert werden muss und keine Änderungen an zugeordneten Befehls Handlern im Kern Anwendungscode vorgenommen werden, überarbeiten Sie die Markup Quelldatei, kompilieren Sie das Markup mit UICC.exe neu, und verknüpfen Sie die neuen Markup Ressourcen Dateien. Wenn die Anwendung neu gestartet wird, wird die geänderte Benutzeroberfläche angezeigt.

All dies ist möglich, ohne den Kern Anwendungscode zu berühren – eine bedeutende Verbesserung im Vergleich zur standardmäßigen Anwendungsentwicklung und-Verteilung.

## <a name="run-time-updates-and-executions"></a>Lauf Zeit Updates und Ausführungen

Die Lauf Zeit Kommunikationsstruktur des Menüband-Frameworks basiert auf einem Push-und Pull-oder bidirektionalen Aufrufer-Modell.

Dieses Modell ermöglicht es dem Framework, die Anwendung zu informieren, wenn ein Befehl ausgeführt wird, und ermöglicht sowohl dem Framework als auch der Anwendung das Abfragen, aktualisieren und ungültig machen von Eigenschafts Werten und Menü Band Ressourcen. Diese Funktionalität wird durch eine Reihe von Schnittstellen und Methoden bereitgestellt.

Das Framework ruft aktualisierte Eigenschaften Informationen mithilfe der [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode aus der Multifunktionsleisten-Anwendung ab. Eine Befehls-ID und ein Eigenschafts Schlüssel, der die zu Aktualisier Endes Befehls Eigenschaft identifiziert, werden an die Methode weitergegeben, die dann einen Wert für diesen Eigenschafts Schlüssel an das Framework zurückgibt oder diesen überträgt.

Das Framework ruft [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) auf, wenn ein Befehl ausgeführt wird, wobei sowohl die Befehls-ID als auch der aufgetretene Typ der Ausführung ([**UI \_ executionverb**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)) identifiziert wird. An dieser Stelle gibt die Anwendung die Ausführungs Logik für einen Befehl an.

Das folgende Diagramm veranschaulicht die Lauf Zeit Kommunikation für die Befehlsausführung zwischen dem Framework und der Anwendung.

![das Diagramm zeigt ein Beispiel für die Lauf Zeit Kommunikation zwischen dem Menüband-Framework und einer Host Anwendung.](images/overviews/updatesandexecutions.png)

> [!Note]  
> Das Implementieren der [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Funktion und der [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Funktion ist nicht erforderlich, um anfänglich ein Menüband in einer Anwendung anzuzeigen. Diese Methoden sind jedoch erforderlich, um sicherzustellen, dass die Anwendung ordnungsgemäß funktioniert, wenn Befehle vom Benutzer ausgeführt werden.

 

## <a name="ole-support"></a>OLE-Unterstützung

Eine Menüband-Anwendung kann als OLE-Server konfiguriert werden, um die Out-of-Place-OLE-Aktivierung zu unterstützen.

Objekte, die in einer OLE-Serveranwendung erstellt wurden, behalten ihre Zuordnung mit der Serveranwendung bei, wenn Sie in eine OLE-Client Anwendung (oder in einen Container) eingefügt (oder eingefügt) werden. Bei der Out-of-Place-OLE-Aktivierung wird durch Doppelklicken auf das Objekt in der Client Anwendung eine dedizierte Instanz der Serveranwendung geöffnet, und das Objekt wird zur Bearbeitung geladen. Wenn die Serveranwendung geschlossen wird, werden alle an dem Objekt vorgenommenen Änderungen in der Client Anwendung übernommen.

> [!Note]  
> Das Menüband-Framework unterstützt keine direkte OLE-Aktivierung. Objekte, die in einem Menüband-basierten OLE-Server erstellt werden, können nicht innerhalb der OLE-Client Anwendung bearbeitet werden. Eine externe dedizierte Instanz der Serveranwendung ist erforderlich.


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup](./windowsribbon-schema.md)
</dt> <dt>

[Multifunktionsleisten-Benutzeroberflächen Richtlinien](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Menüband-Entwurfsprozess](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




