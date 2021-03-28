---
description: Veranschaulicht, wie ein shellverb mithilfe der ExecuteCommand-Methode implementiert wird.
title: „Befehl ausführen“-Verb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2deeb63fc6648d07b3d870888d6d2eabc6fb0490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218709"
---
# <a name="execute-command-verb-sample"></a>„Befehl ausführen“-Verb (Beispiel)

Veranschaulicht, wie ein shellverb mithilfe der ExecuteCommand-Methode implementiert wird.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="description"></a>BESCHREIBUNG

Diese Methode wird für Verb Implementierungen bevorzugt, da Sie die größtmögliche Flexibilität bietet, einfach ist und die Prozess interne Aktivierung unterstützt. In diesem Beispiel wird ein eigenständiges com-Objekt (Local Server Component Object Model) implementiert. es wird jedoch erwartet, dass die Verb-Implementierung in vorhandene Anwendungen integriert wird. Zu diesem Zweck muss das Haupt Anwendungs Objekt eine Klassenfactory für sich selbst registrieren. Dieses Objekt implementiert [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) für die Verben Ihrer Anwendung. Beachten Sie, dass die Anwendung von com gestartet wird, wenn Sie nicht bereits ausgeführt wird, sondern eine Verbindung mit einer laufenden Instanz der Anwendung herstellt, wenn eine vorhanden ist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Produkt                                | Minimale Produkt Version |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Executecommandverb-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **executecommandverb** .
2.  Geben Sie `msbuild ExecuteCommand.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **executecommandverb** .
2.  Doppelklicken Sie auf das Symbol für die Datei ExecuteCommand. sln, um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie in der Befehlszeile ein `ExecuteCommand.exe` . Alternativ können Sie in Windows-Explorer auf das Symbol für ExecuteCommand.exe doppelklicken.
3.  Befolgen Sie die Anweisungen im angezeigten Dialogfeld.

 

 
