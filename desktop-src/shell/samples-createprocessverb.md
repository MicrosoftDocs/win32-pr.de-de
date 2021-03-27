---
description: Veranschaulicht die Implementierung eines shellverbs mithilfe der Methode "Methode".
title: CreateProcess-Verb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e52f251e12f0ca06bcb729407a7c8303836f9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980329"
---
# <a name="createprocess-verb-sample"></a>CreateProcess-Verb (Beispiel)

Veranschaulicht die Implementierung eines shellverbs mithilfe der Methode "Methode".

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="description"></a>BESCHREIBUNG

Auf dem Prozess basierende Verben sind von der Ausführung einer ausführbaren Datei und der Übergabe eines Befehlszeilen Arguments abhängig. Diese Methode ist nicht so leistungsfähig wie die Methoden "DropTarget" und "ExecuteCommand", aber Sie erreicht das wünschenswert Verhalten außerhalb des Prozesses.

## <a name="requirements"></a>Requirements (Anforderungen)



| Produkt                                | Minimale Produkt Version |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Beispiel für "kreateprocessverb"](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie **zum Projektverzeichnis** für das Projekt "Projekt".
2.  Geben Sie `msbuild CreateProcessVerb.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie **zum Projektverzeichnis** für das Projekt "Projekt".
2.  Doppelklicken Sie auf das Symbol für die Datei "Datei" in Visual Studio, um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie in der Befehlszeile ein `CreateProcessVerb.exe` . Alternativ können Sie in Windows-Explorer auf das Symbol für CreateProcessVerb.exe doppelklicken.
3.  Befolgen Sie die Anweisungen im angezeigten Dialogfeld.

 

 



