---
description: Veranschaulicht, wie ein shellverb mithilfe der Methoden explorercommand und explorercommandstate implementiert wird.
title: Explorer-Befehl-Verb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a35662c3df0e0fcddae049ccfaac2d9e3e265ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868304"
---
# <a name="explorer-command-verb-sample"></a>Explorer-Befehl-Verb (Beispiel)

Veranschaulicht, wie ein shellverb mithilfe der Methoden explorercommand und explorercommandstate implementiert wird.

Dieses Thema enthält folgende Abschnitte:

-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="requirements"></a>Requirements (Anforderungen)



| Produkt                                | Minimale Produkt Version |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Explorercommandverb-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **explorercommandverb** .
2.  Geben Sie `msbuild ExplorerCommandVerb.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **explorercommandverb** .
2.  Doppelklicken Sie auf das Symbol für die Datei explorercommandverb. sln, um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die ExplorerCommandVerb.dll enthält. Stellen Sie sicher, dass Sie die 64-Bit-DLL-Datei auf 64-Bit-Windows verwenden.
2.  Geben Sie in der Befehlszeile ein `regsvr32.exe ExplorerCommandVerb.dll` .
3.  Wenn Sie mit der rechten Maustaste auf eine txt-Datei klicken, werden zwei neue Verben im Kontextmenü angezeigt.

 

 



