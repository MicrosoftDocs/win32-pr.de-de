---
description: Veranschaulicht, wie eine Shellnamespaceerweiterung implementiert wird, einschließlich Kontextmenüverhalten und benutzerdefinierter Aufgaben im Browser.
title: Explorer-Datenanbieter (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 31e1d42e4660e0e73830876cfdeb0a5c8a5957cd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471886"
---
# <a name="explorer-data-provider-sample"></a>Explorer-Datenanbieter (Beispiel)

Veranschaulicht, wie eine Shellnamespaceerweiterung implementiert wird, einschließlich Kontextmenüverhalten und benutzerdefinierter Aufgaben im Browser.

Dieses Thema enthält folgende Abschnitte:

-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="requirements"></a>Anforderungen



| Produkt                                | Mindestversion des Produkts |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 6.1                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Position      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [ExplorerDataProvider-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum Projektverzeichnis **ExplorerDataProvider.**
2.  Geben Sie `msbuild ExplorerDataProvider.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows Explorer, und navigieren Sie zum Projektverzeichnis **ExplorerDataProvider.**
2.  Doppelklicken Sie auf das Symbol für die Datei ExplorerDataProvider.sln, um das Projekt in Visual Studio zu öffnen.
3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen). Die DLL wird im \\ Standardverzeichnis Debug oder \\ Release erstellt.

> [!Note]  
> In der Version dieses Beispiels, die im Windows SDK enthalten ist, enthält die Konfiguration für den 64-Bit-Releasebuild nicht die Datei ExplorerDataProvider.def in der Option **Moduldefinitionsdatei** des Linkers. Sie müssen diese Datei selbst angeben, bevor Sie in einer 64-Bit-Umgebung erstellen. Fügen Sie die Zeile `ModuleDefinitionFile="ExplorerDataProvider.def"` dem VcLinkerTool-Abschnitt (beginnt bei Zeile 329) der Datei ExplorerDataProvider.vcproj hinzu, wie hier gezeigt:
>
> <span codelanguage=""></span>
>
> 
| | | <pre><code>LinkIncremental="1"&gt; AdditionalLibraryDirectories=""c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64""&gt; ModuleDefinitionFile="ExplorerDataProvider.def"&gt; GenerateDebugInformation="true"</code></pre> | 

>
> 
>
> Die Version dieses Beispiels, die aus dem Codekatalog heruntergeladen werden kann, wurde für dieses Problem korrigiert, und Es ist keine zusätzliche Aktion erforderlich.
>
>  
>
> ## <a name="running-the-sample"></a>Ausführen des Beispiels
>
> 1.  Navigieren Sie über die Eingabeaufforderung oder Windows Explorer zu dem Verzeichnis, das die neue .dll- und PROPDESC-Datei enthält.
> 2.  Geben Sie in der Befehlszeile `regsvr32.exe` ein.
>     > [!Note]  
>     > Wenn Sie diesen Befehl über eine Eingabeaufforderung mit erhöhten Rechten ausführen, registriert die Selbstregistrierung auch automatisch die PROPDESC-Datei. Wenn sie über eine Eingabeaufforderung ohne erhöhte Rechte ausgeführt wird, funktioniert die Namespaceerweiterung, jedoch ohne benutzerdefinierte Eigenschaftenfunktionalität.
>
>      
>
> 3.  Öffnen Sie den **Ordner Arbeitsplatz,** und durchsuchen Sie die neue Namespaceerweiterung, die dort vorhanden ist.
>
>  
>
>  
>


