---
description: Veranschaulicht, wie ein Shellverb mithilfe der Methoden ExplorerCommand und ExplorerCommandState implementiert wird.
title: Explorer-Befehl-Verb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2310A6AA-EAF9-4d7a-A784-04931BDC2089
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ec8f4c88ea01aad410e982fc24fd248f3c1826d8c8657e904844b535e621fd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719182"
---
# <a name="explorer-command-verb-sample"></a>Explorer-Befehl-Verb (Beispiel)

Veranschaulicht, wie ein Shellverb mithilfe der Methoden ExplorerCommand und ExplorerCommandState implementiert wird.

Dieses Thema enthält folgende Abschnitte:

-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="requirements"></a>Anforderungen



| Product (Produkt)                                | Mindestversion des Produkts |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [ExplorerCommandVerb-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExplorerCommandVerb) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum Projektverzeichnis **ExplorerCommandVerb.**
2.  Geben Sie `msbuild ExplorerCommandVerb.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows Explorer, und navigieren Sie zum Projektverzeichnis **ExplorerCommandVerb.**
2.  Doppelklicken Sie auf das Symbol für die Datei ExplorerCommandVerb.sln, um das Projekt in Visual Studio zu öffnen.
3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows Explorer zu dem Verzeichnis, das die ExplorerCommandVerb.dll enthält. Stellen Sie sicher, dass Sie die 64-Bit-DLL-Datei auf 64-Bit-Windows verwenden.
2.  Geben Sie in der Befehlszeile `regsvr32.exe ExplorerCommandVerb.dll` ein.
3.  Zwei neue Verben werden im Kontextmenü angezeigt, wenn Sie mit der rechten Maustaste auf eine .txt Datei klicken.

 

 



