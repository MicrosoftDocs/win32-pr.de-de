---
description: Das propertyedit-Codebeispiel veranschaulicht, wie Sie den kanonischen Eigenschaftsnamen in einen PropertyKey konvertieren, den Wert des Eigenschaften Speicher auf den des Elements festlegen und die Daten zurück in den Dateistream schreiben.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa248b9e86f8ab93cccba3d5d6b169d7e8699dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862167"
---
# <a name="propertyedit"></a>PropertyEdit

Das propertyedit-Codebeispiel veranschaulicht, wie Sie den kanonischen Eigenschaftsnamen in einen PropertyKey konvertieren, den Wert des Eigenschaften Speicher auf den des Elements festlegen und die Daten zurück in den Dateistream schreiben.

Dieses Thema enthält folgende Abschnitte:

-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Anforderungen



| Produkt     | Minimale Produkt Version |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist in den folgenden Speicherorten verfügbar.



| Standort      | Pfad-URL                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [Propertyedit-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> Für alle Versionen von Windows, einschließlich Windows 7, empfiehlt es sich, die Beispiele direkt von GitHub für die aktuellste Version herunterzuladen.

 

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **propertyedit** . 
2.  Geben Sie `msbuild PropertyEdit.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **propertyedit** .
2.  Doppelklicken Sie auf das Symbol für die Datei propertyedit. sln, um das Projekt in Visual Studio zu öffnen.
    > [!Note]  
    > Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt. In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.

     

3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mit dem Eingabe Aufforderungs Fenster oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie an der Eingabeaufforderung ein, `PropertyEdit.exe` oder Doppelklicken Sie in Windows-Explorer auf das Symbol für PropertyEdit.exe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Code Beispiele durchsuchen](-search-samples-ovw.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[Informationen zu Eigenschaften und Eigenschaften Handlern](../properties/building-property-handlers-properties.md)
</dt> <dt>

[Eigenschafts Beschreibungs Schema](/previous-versions//cc144127(v=vs.85))
</dt> </dl>

 

 
