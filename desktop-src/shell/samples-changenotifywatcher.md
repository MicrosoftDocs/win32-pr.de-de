---
description: Veranschaulicht das Lauschen auf shelländerungbenachrichtigungen für einen Ordner oder ein Element im Windows Explorer-Namespace.
title: Benachrichtigungsüberwachung ändern (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 02A7C5B4-94F2-4c35-9290-4C816E5CF63A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5d0ac6ccb2dd2328d81b77d03bffc68dfa9a70cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217208"
---
# <a name="change-notify-watcher-sample"></a>Benachrichtigungsüberwachung ändern (Beispiel)

Veranschaulicht das Lauschen auf shelländerungbenachrichtigungen für einen Ordner oder ein Element im Windows Explorer-Namespace.

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
| GitHub  | [Changenotifywatcher-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis " **changenotifywatcher** ".
2.  Geben Sie `msbuild ChangeNotifyWatcher.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis " **changenotifywatcher** ".
2.  Doppelklicken Sie auf das Symbol für die Datei "changenotifywatcher. sln", um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie an der Eingabeaufforderung `ChangeNotifyWatcher.exe` ein. Alternativ können Sie in Windows-Explorer auf das Symbol für ChangeNotifyWatcher.exe doppelklicken.
3.  Um die Auswirkung zu veranschaulichen, wählen App-Benutzer Modell-IDs (appusermudelids) einen zu überwachenden Ordner aus, indem Sie entweder auf **"Pick..."** klicken oder Drag & amp; Drop für einen Ordner aus einem Windows-Explorer-Fenster in die Listenansicht des Beispiels anwenden.

 

 



