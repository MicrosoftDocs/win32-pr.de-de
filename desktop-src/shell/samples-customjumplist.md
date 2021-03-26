---
description: Veranschaulicht, wie eine benutzerdefinierte Sprung Liste für eine Anwendung erstellt wird, einschließlich Hinzufügen einer benutzerdefinierten Kategorie und Aufgaben.
title: Benutzerdefinierte Sprungliste (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c20592e508a24985e0f8283993482c7bd61af232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217206"
---
# <a name="custom-jump-list-sample"></a>Benutzerdefinierte Sprungliste (Beispiel)

Veranschaulicht, wie eine benutzerdefinierte Sprung Liste für eine Anwendung erstellt wird, einschließlich Hinzufügen einer benutzerdefinierten Kategorie und Aufgaben.

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
| GitHub  | [Customjumplist-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **customjumplist** .
2.  Geben Sie `msbuild CustomJumpListSample.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **customjumplist** .
2.  Doppelklicken Sie auf das Symbol für die Datei customjumplistsample. sln, um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie in der Befehlszeile ein `CustomJumpListSample.exe` . Alternativ können Sie in Windows-Explorer auf das Symbol für CustomJumpListSample.exe doppelklicken.
3.  Dieses Beispiel muss bei der erstmaligen Durchführung als Administrator ausgeführt werden, damit die erforderlichen Dateityp Registrierungen installiert werden können. Nachdem die Dateitypen registriert wurden, kann das Beispiel als Standardbenutzer ausgeführt werden.
4.  Wählen Sie Optionen aus dem Menü in der Beispielanwendung aus, um zu sehen, wie Sie sich auf die Sprung Liste der Anwendung in der Taskleiste auswirken.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Benutzer Modell-IDs (appusermudelids)](appids.md)
</dt> </dl>

 

 



