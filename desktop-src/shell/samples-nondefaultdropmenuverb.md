---
description: Veranschaulicht das Erweitern des Drag & Drop-Kontextmenüs (manchmal auch als Kontextmenü bezeichnet).
title: NonDefaultDropMenuVerb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1c4623b9143e0a23762cfc44dd8dfc4f46b827a0f6433098d45d8a784ead81f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968789"
---
# <a name="nondefaultdropmenuverb-sample"></a>NonDefaultDropMenuVerb (Beispiel)

Veranschaulicht das Erweitern des Drag & Drop-Kontextmenüs (manchmal auch als Kontextmenü bezeichnet).

Dieses Thema enthält folgende Abschnitte:

-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="requirements"></a>Anforderungen



| Product (Produkt)                                | Mindestproduktversion |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [NonDefaultDropMenuVerb-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum **Projektverzeichnis NonDefaultDropMenuVerb.**
2.  Geben Sie `msbuild NonDefaultDropMenuVerb.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Windows Explorer, und navigieren Sie zum **Projektverzeichnis NonDefaultDropMenuVerb.**
2.  Doppelklicken Sie auf das Symbol für die Datei NonDefaultDropMenuVerb.sln, um das Projekt in Visual Studio.
3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie über die Eingabeaufforderung oder den Explorer zu dem Verzeichnis, das die neue DLL-Windows enthält.
2.  Kopieren NonDefaultDropMenuVerb.dll in das Verzeichnis System (z. B. C: \\ Windows \\ System32).
3.  Geben Sie an einer Eingabeaufforderung `regedit NonDefaultDropMenuVerb.reg` ein.
4.  Verwenden Sie die rechte Maustaste, um eine Datei von einem Ordner in einen anderen zu ziehen. Für den Abbruchvorgang werden zusätzliche Menüelemente angezeigt.

 

 



