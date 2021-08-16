---
description: Veranschaulicht, wie ein Shellverb mithilfe der ExecuteCommand-Methode implementiert wird.
title: „Befehl ausführen“-Verb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e32b472d63b9d2d779c97b64833f354e7d4d2eaed034d3a213ae4e101f7beb3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858269"
---
# <a name="execute-command-verb-sample"></a>„Befehl ausführen“-Verb (Beispiel)

Veranschaulicht, wie ein Shellverb mithilfe der ExecuteCommand-Methode implementiert wird.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="description"></a>Beschreibung

Diese Methode wird für Verbimplementierungen bevorzugt, da sie die größte Flexibilität bietet, einfach ist und die Out-of-Process-Aktivierung unterstützt. In diesem Beispiel wird ein eigenständiges, lokales COMPONENT OBJECT MODEL(COM)-Objekt implementiert, aber es wird erwartet, dass die Verbimplementierung in vorhandene Anwendungen integriert wird. Zu diesem Grund muss ihr Hauptanwendungsobjekt eine Klassen factory für sich selbst registrieren. Dieses Objekt implementiert [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) für die Verben Ihrer Anwendung. Beachten Sie, dass COM Ihre Anwendung startet, wenn sie noch nicht ausgeführt wird, aber eine Verbindung mit einer ausgeführten Instanz Ihrer Anwendung herstellt, sofern vorhanden.

## <a name="requirements"></a>Anforderungen



| Product (Produkt)                                | Mindestproduktversion |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [ExecuteCommandVerb-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum **Projektverzeichnis ExecuteCommandVerb.**
2.  Geben Sie `msbuild ExecuteCommand.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Windows Explorer, und navigieren Sie zum **Projektverzeichnis ExecuteCommandVerb.**
2.  Doppelklicken Sie auf das Symbol für die Datei ExecuteCommand.sln, um das Projekt in Visual Studio.
3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie über die Eingabeaufforderung oder den Explorer zu dem Verzeichnis, das die neue ausführbare Windows enthält.
2.  Geben Sie in der Befehlszeile `ExecuteCommand.exe` ein. Doppelklicken Sie alternativ Windows Explorer auf das Symbol für ExecuteCommand.exe.
3.  Befolgen Sie die Anweisungen im angezeigten Dialogfeld.

 

 
