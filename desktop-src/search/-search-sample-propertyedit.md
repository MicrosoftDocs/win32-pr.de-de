---
description: Im Codebeispiel PropertyEdit wird veranschaulicht, wie sie den kanonischen Eigenschaftennamen in einen PROPERTYKEY konvertieren, den Wert des Eigenschaftenspeichers auf den wert des Elements festlegen und die Daten in den Dateistream zurückschreiben.
ms.assetid: 5918b4f6-6b6f-4229-8f29-1c41f80b3b02
title: PropertyEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944419f990c8f1f8b52706dbab0b08102829e77a5bfa8a91c72a5bc16eddfa63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944669"
---
# <a name="propertyedit"></a>PropertyEdit

Im Codebeispiel PropertyEdit wird veranschaulicht, wie sie den kanonischen Eigenschaftennamen in einen PROPERTYKEY konvertieren, den Wert des Eigenschaftenspeichers auf den wert des Elements festlegen und die Daten in den Dateistream zurückschreiben.

Dieses Thema enthält folgende Abschnitte:

-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="requirements"></a>Anforderungen



| Product (Produkt)     | Mindestproduktversion |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Windows SDK | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort      | Pfad-URL                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [PropertyEdit-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/PropertyEdit)    |



 

 

> [!Note]  
> Für alle Versionen von Windows, einschließlich Windows 7, wird empfohlen, die Beispiele für die aktuelle Version direkt von GitHub herunterzuladen.

 

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum **Projektverzeichnis PropertyEdit.** 
2.  Geben Sie `msbuild PropertyEdit.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Windows Explorer, und navigieren Sie zum **Projektverzeichnis PropertyEdit.**
2.  Doppelklicken Sie auf das Symbol für die Datei PropertyEdit.sln, um das Projekt in Visual Studio.
    > [!Note]  
    > Die Dateierweiterung SLN wird unter den Standardordnereinstellungen nicht angezeigt. In diesem Fall kann er anhand seines eindeutigen Symbols oder seiner Typbeschreibung "Microsoft Visual Studio identifiziert werden.

     

3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie zum Verzeichnis, das die neue ausführbare Datei enthält, indem Sie das Eingabeaufforderungsfenster oder den Windows verwenden.
2.  Geben Sie an der Eingabeaufforderung ein, oder doppelklicken Sie Windows Explorer auf das Symbol `PropertyEdit.exe` für PropertyEdit.exe.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Suchcodebeispiele](-search-samples-ovw.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> <dt>

[Informationen zu Eigenschaften und Eigenschaftenhandlern](../properties/building-property-handlers-properties.md)
</dt> <dt>

[Schema der Eigenschaftenbeschreibung](/previous-versions//cc144127(v=vs.85))
</dt> </dl>

 

 
