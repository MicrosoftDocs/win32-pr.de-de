---
description: Veranschaulicht das Hinzufügen von Elementen zum automatischen Sprungliste für eine Anwendung, einschließlich des Wechsels zwischen der Anzeige der Kategorien Häufig und Zuletzt angezeigt.
title: Beispiel für eine automatische Sprungliste
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4dcb2146c8db8eda0280b3ff7a34a19faf4ac172036ae7a4e61131b50fde2d0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090190"
---
# <a name="automatic-jump-list-sample"></a>Beispiel für eine automatische Sprungliste

Veranschaulicht das Hinzufügen von Elementen zum automatischen Sprungliste für eine Anwendung, einschließlich des Wechsels zwischen der Anzeige der Kategorien Häufig und Zuletzt angezeigt.

Dieses Thema enthält folgende Abschnitte:

-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Anforderungen



| Product (Produkt)                                | Mindestversion des Produkts |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [AutomaticJumpList-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum Projektverzeichnis **AutomaticJumpList.**
2.  Geben Sie `msbuild AutomaticJumpListSample.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows Explorer, und navigieren Sie zum Projektverzeichnis **AutomaticJumpList.**
2.  Doppelklicken Sie auf das Symbol für die Datei AutomaticJumpListSample.sln, um das Projekt in Visual Studio zu öffnen.
3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie über die Eingabeaufforderung oder Windows Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie in der Befehlszeile `AutomaticJumpListSample.exe` ein. Alternativ können Sie Windows Explorer auf das Symbol für AutomaticJumpListSample.exe doppelklicken.
3.  Dieses Beispiel muss bei der ersten Ausführung als Administrator ausgeführt werden, damit die erforderlichen Dateitypregistrierungen installiert werden können. Nachdem die Dateitypen registriert wurden, kann das Beispiel als Standardbenutzer ausgeführt werden.
4.  Wählen Sie optionen aus dem Menü in der Beispielanwendung aus, einschließlich der Auswahl von .txt oder .doc Dokumente über das Dialogfeld **Öffnen,** um zu sehen, wie sie sich auf die Sprungliste der Anwendung in der Taskleiste auswirken.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsbenutzermodell-IDs (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 



