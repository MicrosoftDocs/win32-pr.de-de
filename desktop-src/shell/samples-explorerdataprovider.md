---
description: Veranschaulicht, wie eine Shell-Namespace Erweiterung implementiert wird, einschließlich Kontextmenü Verhalten und benutzerdefinierter Aufgaben im Browser.
title: Explorer-Datenanbieter (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6bd15cbef62ff69efcccd28fcb625fc1432fdf89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218062"
---
# <a name="explorer-data-provider-sample"></a>Explorer-Datenanbieter (Beispiel)

Veranschaulicht, wie eine Shell-Namespace Erweiterung implementiert wird, einschließlich Kontextmenü Verhalten und benutzerdefinierter Aufgaben im Browser.

Dieses Thema enthält folgende Abschnitte:

-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="requirements"></a>Requirements (Anforderungen)



| Produkt                                | Minimale Produkt Version |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 6.1                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Explorerdataprovider-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **explorerdataprovider** .
2.  Geben Sie `msbuild ExplorerDataProvider.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **explorerdataprovider** .
2.  Doppelklicken Sie auf das Symbol für die Datei explorerdataprovider. sln, um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus. Die dll wird im standardmäßigen Debug- \\ oder \\ releaseverzeichnis erstellt.

> [!Note]  
> In der Version dieses Beispiels, das in der Windows SDK enthalten ist, enthält die Konfiguration für den Build der 64-Bit-Version nicht die Datei "explorerdataprovider. def" in der **Modul Definitionsdatei** -Option des Linkers. Sie müssen diese Datei vor dem Aufbau in einer 64-Bit-Umgebung selbst angeben. Fügen Sie die Zeile `ModuleDefinitionFile="ExplorerDataProvider.def"` zum Abschnitt "VCLinkerTool" (beginnt in Zeile 329) der Datei "explorerdataprovider. vcproj" hinzu, wie hier gezeigt:
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
> Die Version dieses Beispiels, die aus der Code Gallery heruntergeladen werden kann, wurde für dieses Problem korrigiert, und es sind keine weiteren Aktionen erforderlich.
>
>  
>
> ## <a name="running-the-sample"></a>Ausführen des Beispiels
>
> 1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue dll-und PropDesc-Datei enthält.
> 2.  Geben Sie in der Befehlszeile ein `regsvr32.exe` .
>     > [!Note]  
>     > Wenn Sie diesen Befehl an einer Eingabeaufforderung mit erhöhten Rechten ausführen, wird die Datei ". PropDesc" auch automatisch von der Selbstregistrierung registriert. Wenn Sie an einer Eingabeaufforderung ohne erhöhte Rechte ausgeführt wird, funktioniert die Namespace Erweiterung, aber ohne benutzerdefinierte Eigenschafts Funktionalität.
>
>      
>
> 3.  Öffnen Sie den Ordner **Arbeitsplatz** , und Durchsuchen Sie die neue Namespace Erweiterung vorhanden.
>
>  
>
>  
>


