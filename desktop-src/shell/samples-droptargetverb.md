---
description: Veranschaulicht, wie ein Shellverb mithilfe der DropTarget-Methode implementiert wird.
title: DropTarget-Verb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ae9ae3edb2d993f2e42a2556899d45cb3b10722fc7d7a9dc5e9786560fc3078f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719532"
---
# <a name="droptarget-verb-sample"></a>DropTarget-Verb (Beispiel)

Veranschaulicht, wie ein Shellverb mithilfe der DropTarget-Methode implementiert wird.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="description"></a>Beschreibung

In diesem Beispiel wird gezeigt, wie Ein Shell-Verb mithilfe der DropTarget-Methode implementiert wird. Diese Methode wird für Verbimplementierungen bevorzugt, die auf Windows XP funktionieren müssen. Dieses Beispiel implementiert einen eigenständigen lokalen Server Component Object Model -Objekt (COM), es wird jedoch erwartet, dass die Verbimplementierungen in vorhandene Anwendungen integriert werden. Zu diesem Zweck registriert Ihr Hauptanwendungsobjekt eine Klassenfactory für sich selbst. Dieses Objekt implementiert [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) für die Verben Ihrer Anwendung. Beachten Sie, dass COM Ihre Anwendung startet, wenn sie nicht bereits ausgeführt wird, aber eine Verbindung mit einer ausgeführten Instanz Ihrer Anwendung herstellt, sofern vorhanden.

## <a name="requirements"></a>Anforderungen



| Product (Produkt)                                | Mindestversion des Produkts |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [DropTargetVerb-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum Projektverzeichnis **DropTargetVerb.**
2.  Geben Sie `msbuild DropTargetVerb.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows Explorer, und navigieren Sie zum Projektverzeichnis **DropTargetVerb.**
2.  Doppelklicken Sie auf das Symbol für die Datei DropTargetVerb.sln, um das Projekt in Visual Studio zu öffnen.
3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie über die Eingabeaufforderung oder Windows Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie in der Befehlszeile `DropTargetVerb.exe` ein. Alternativ können Sie in Windows Explorer auf das Symbol für DropTargetVerb.exe doppelklicken.
3.  Befolgen Sie die Anweisungen im angezeigten Dialogfeld.

 

 
