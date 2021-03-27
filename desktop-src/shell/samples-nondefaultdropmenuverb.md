---
description: Veranschaulicht, wie das Kontextmenü für Drag & amp; Drop (manchmal auch als Kontextmenü bezeichnet) erweitert wird.
title: NonDefaultDropMenuVerb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9d326e012fb78b04fd542f88d49c370e8aeab613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347929"
---
# <a name="nondefaultdropmenuverb-sample"></a>NonDefaultDropMenuVerb (Beispiel)

Veranschaulicht, wie das Kontextmenü für Drag & amp; Drop (manchmal auch als Kontextmenü bezeichnet) erweitert wird.

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
| GitHub  | [Nondefaultdropmenuverb-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **nondefaultdropmenuverb** .
2.  Geben Sie `msbuild NonDefaultDropMenuVerb.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **nondefaultdropmenuverb** .
2.  Doppelklicken Sie auf das Symbol für die Datei nondefaultdropmenuverb. sln, um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue dll-Datei enthält.
2.  Kopieren Sie NonDefaultDropMenuVerb.dll in das System Verzeichnis (z. b. C: \\ Windows \\ system32).
3.  Geben Sie an einer Eingabeaufforderung ein `regedit NonDefaultDropMenuVerb.reg` .
4.  Ziehen Sie mit der rechten Maustaste eine Datei aus einem Ordner in einen anderen. Weitere Menü Elemente für den Drop-Vorgang werden angezeigt.

 

 



