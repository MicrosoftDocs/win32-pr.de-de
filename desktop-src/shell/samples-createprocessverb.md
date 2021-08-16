---
description: Veranschaulicht, wie ein Shellverb mithilfe der CreateProcess-Methode implementiert wird.
title: CreateProcess-Verb (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c0af34d5ec9f687ec6c58bb73f337b38d512527c0ace4bd20eae12d49c87a62d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858340"
---
# <a name="createprocess-verb-sample"></a>CreateProcess-Verb (Beispiel)

Veranschaulicht, wie ein Shellverb mithilfe der CreateProcess-Methode implementiert wird.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="description"></a>BESCHREIBUNG

CreateProcess-basierte Verben hängen davon ab, dass eine ausführbare Datei ausgeführt und ein Befehlszeilenargument übergeben wird. Diese Methode ist nicht so leistungsfähig wie die DropTarget- und ExecuteCommand-Methoden, erreicht jedoch das gewünschte Out-of-Process-Verhalten.

## <a name="requirements"></a>Anforderungen



| Product (Produkt)                                | Mindestproduktversion |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [CreateProcessVerb-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum **Projektverzeichnis CreateProcessVerb.**
2.  Geben Sie `msbuild CreateProcessVerb.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Windows Explorer, und navigieren Sie zum **Projektverzeichnis CreateProcessVerb.**
2.  Doppelklicken Sie auf das Symbol für die Datei CreateProcessVerb.sln, um das Projekt in Visual Studio.
3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie über die Eingabeaufforderung oder den Explorer zu dem Verzeichnis, das die neue ausführbare Windows enthält.
2.  Geben Sie in der Befehlszeile `CreateProcessVerb.exe` ein. Doppelklicken Sie alternativ Windows Explorer auf das Symbol für CreateProcessVerb.exe.
3.  Befolgen Sie die Anweisungen im angezeigten Dialogfeld.

 

 



