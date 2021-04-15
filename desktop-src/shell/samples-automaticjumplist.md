---
description: Veranschaulicht das Hinzufügen von Elementen zur automatischen Sprung Liste für eine Anwendung, einschließlich des Wechsels zwischen der Anzeige der häufig und der aktuellen Kategorie.
title: Beispiel für eine automatische Sprungliste
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ce0b6520163fcb07bb990b7a5a9fe742d976a899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485563"
---
# <a name="automatic-jump-list-sample"></a>Beispiel für eine automatische Sprungliste

Veranschaulicht das Hinzufügen von Elementen zur automatischen Sprung Liste für eine Anwendung, einschließlich des Wechsels zwischen der Anzeige der häufig und der aktuellen Kategorie.

Dieses Thema enthält folgende Abschnitte:

-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Requirements (Anforderungen)



| Produkt                                | Minimale Produkt Version |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Automaticjumplist-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **automaticjumplist** .
2.  Geben Sie `msbuild AutomaticJumpListSample.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **automaticjumplist** .
2.  Doppelklicken Sie auf das Symbol für die Datei automaticjumplistsample. sln, um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie in der Befehlszeile ein `AutomaticJumpListSample.exe` . Alternativ können Sie in Windows-Explorer auf das Symbol für AutomaticJumpListSample.exe doppelklicken.
3.  Dieses Beispiel muss bei der erstmaligen Durchführung als Administrator ausgeführt werden, damit die erforderlichen Dateityp Registrierungen installiert werden können. Nachdem die Dateitypen registriert wurden, kann das Beispiel als Standardbenutzer ausgeführt werden.
4.  Wählen Sie Optionen aus dem Menü in der Beispielanwendung aus, einschließlich der Auswahl von txt-oder doc-Dokumenten über das Dialogfeld **Öffnen** , um zu sehen, wie Sie sich auf die Sprung Liste der Anwendung in der Taskleiste auswirken.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Benutzer Modell-IDs (appusermudelids)](appids.md)
</dt> </dl>

 

 



