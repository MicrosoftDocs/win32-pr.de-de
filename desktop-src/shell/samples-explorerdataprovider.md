---
description: Veranschaulicht, wie eine Shell-Namespaceerweiterung implementiert wird, einschließlich Kontextmenüverhalten und benutzerdefinierter Aufgaben im Browser.
title: Explorer-Datenanbieter (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 223f498f42e33dda09206b1e21a44138fda54e261ec957efb62e55148a014d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677837"
---
# <a name="explorer-data-provider-sample"></a>Explorer-Datenanbieter (Beispiel)

Veranschaulicht, wie eine Shell-Namespaceerweiterung implementiert wird, einschließlich Kontextmenüverhalten und benutzerdefinierter Aufgaben im Browser.

Dieses Thema enthält folgende Abschnitte:

-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="requirements"></a>Anforderungen



| Product (Produkt)                                | Mindestproduktversion |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 6.1                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [ExplorerDataProvider-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum **Projektverzeichnis ExplorerDataProvider.**
2.  Geben Sie `msbuild ExplorerDataProvider.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Windows Explorer, und navigieren Sie zum **Projektverzeichnis ExplorerDataProvider.**
2.  Doppelklicken Sie auf das Symbol für die Datei ExplorerDataProvider.sln, um das Projekt in Visual Studio.
3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen). Die DLL wird im Standardverzeichnis \\ Debuggen oder \\ Release erstellt.

> [!Note]  
> In der Version dieses Beispiels, die im Windows SDK enthalten ist, enthält die Konfiguration für den 64-Bit-Release-Build nicht die Datei ExplorerDataProvider.def in der Option **Moduldefinitionsdatei** des Linkers. Sie müssen diese Datei selbst angeben, bevor Sie in einer 64-Bit-Umgebung erstellen. Fügen Sie die Zeile dem `ModuleDefinitionFile="ExplorerDataProvider.def"` Abschnitt VCLinkerTool (beginnt bei Zeile 329) der Datei ExplorerDataProvider.vcproj hinzu, wie hier gezeigt:
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>LinkIncremental=&quot;1&quot;
> AdditionalLibraryDirectories=&quot;&quot;c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64&quot;&quot;
> ModuleDefinitionFile=&quot;ExplorerDataProvider.def&quot;
> GenerateDebugInformation=&quot;true&quot;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> Die Version dieses Beispiels, die aus dem Codekatalog heruntergeladen werden kann, wurde für dieses Problem behoben, und es ist keine zusätzliche Aktion erforderlich.
>
>  
>
> ## <a name="running-the-sample"></a>Ausführen des Beispiels
>
> 1.  Navigieren Sie über die Eingabeaufforderung oder den .dll Explorer zu dem Verzeichnis Windows, das die neue Datei .dll propdesc enthält.
> 2.  Geben Sie in der Befehlszeile `regsvr32.exe` ein.
>     > [!Note]  
>     > Wenn Sie diesen Befehl über eine Eingabeaufforderung mit erhöhten Rechten ausführen, registriert die Selbstregistrierung automatisch auch die PROPDESC-Datei. Wenn sie über eine Eingabeaufforderung ohne erhöhte Rechte ausgeführt wird, funktioniert die Namespaceerweiterung, jedoch ohne benutzerdefinierte Eigenschaftenfunktionalität.
>
>      
>
> 3.  Öffnen Sie den **Arbeitsplatz,** und durchsuchen Sie die neue Namespaceerweiterung, die dort vorhanden ist.
>
>  
>
>  
>


