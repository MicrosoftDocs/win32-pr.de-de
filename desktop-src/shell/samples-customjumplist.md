---
description: Veranschaulicht das Erstellen eines benutzerdefinierten Sprungliste für eine Anwendung, einschließlich des Hinzufügens einer benutzerdefinierten Kategorie und von Aufgaben.
title: Benutzerdefinierte Sprungliste (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb6f5db0b9576f360abcbaacb8a8a5a291d3dbe07754281954ea585d3ebe965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968829"
---
# <a name="custom-jump-list-sample"></a>Benutzerdefinierte Sprungliste (Beispiel)

Veranschaulicht das Erstellen eines benutzerdefinierten Sprungliste für eine Anwendung, einschließlich des Hinzufügens einer benutzerdefinierten Kategorie und von Aufgaben.

Dieses Thema enthält folgende Abschnitte:

-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Anforderungen



| Product (Produkt)                                | Mindestproduktversion |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [CustomJumpList-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum **Projektverzeichnis CustomJumpList.**
2.  Geben Sie `msbuild CustomJumpListSample.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Windows Explorer, und navigieren Sie zum **Projektverzeichnis CustomJumpList.**
2.  Doppelklicken Sie auf das Symbol für die Datei CustomJumpListSample.sln, um das Projekt in Visual Studio.
3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie über die Eingabeaufforderung oder den Explorer zu dem Verzeichnis, das die neue ausführbare Windows enthält.
2.  Geben Sie in der Befehlszeile `CustomJumpListSample.exe` ein. Doppelklicken Sie alternativ Windows Explorer auf das Symbol für CustomJumpListSample.exe.
3.  Dieses Beispiel muss bei der ersten Ausführung als Administrator ausgeführt werden, damit die erforderlichen Dateitypregistrierungen installiert werden können. Nachdem die Dateitypen registriert wurden, kann das Beispiel als Standardbenutzer ausgeführt werden.
4.  Wählen Sie optionen aus dem Menü in der Beispielanwendung aus, um zu sehen, wie sie sich auf die Sprungliste der Anwendung in der Taskleiste auswirken.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsbenutzermodell-IDs (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 



