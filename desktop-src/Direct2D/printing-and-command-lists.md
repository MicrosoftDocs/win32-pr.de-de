---
title: Druck- und Befehlslisten
description: Das Druck Steuerelement Direct2D \ 32; ist eine neue Komponente im Direct2D-Modul in Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6beb16a24c972016686e2dffe915a947128a63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390440"
---
# <a name="printing-and-command-lists"></a>Druck- und Befehlslisten

Das [Direct2D](./direct2d-portal.md) - [**Druck Steuer**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) Element ist eine neue Komponente im Direct2D-Modul in Windows 8. Mit dieser Komponente können Direct2D-Apps ihre Direct2D-Zeichnungs Aufrufe (hinsichtlich Zustandsänderungen und renderprimitiver) wieder verwenden, um Druckergebnisse zu übermitteln, die mit der Anzeige auf dem Bildschirm vergleichbar sind.

Die [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) -Schnittstelle stellt einen virtuellen Druckauftrag dar: Sie können ein [Direct2D](./direct2d-portal.md) -Druck Steuerelement erstellen, um einen neuen Druckauftrag zu initiieren, Direct2D-Inhalte für jede Seite zu übergeben, die Sie drucken möchten, und dann das Druck Steuerelement schließen, um einen Druckauftrag abzuschließen.

> [!Note]  
> Ein Druck Steuerelement wird einem und genau einem Druckauftrag zugeordnet und kann nicht wieder verwendet werden.

Mit dem Druck Steuerelement [Direct2D](./direct2d-portal.md) wird der übergebene Direct2D-Inhalt für das Druck Subsystem konvertiert und optimiert, das mit den echten Druckern funktioniert, um das tatsächliche PrintOut-Element bereitzustellen. Alle druckspezifischen Details werden in Direct2D-apps ausgeblendet, was bedeutet, dass Direct2D-apps drucken können, ohne zu wissen, auf welche Geräte Sie sich beziehen, oder wie die Zeichnungen in den Druckvorgang übersetzt werden.

Zum Drucken mit [Direct2D](./direct2d-portal.md)müssen Sie eine Direct2D-Befehlsliste für jede Seite vorbereiten, die Sie drucken möchten. übergeben Sie dann die Befehlsliste an das Direct2D-Druck Steuerelement. Um diese Direct2D-Befehlsliste vorzubereiten, erstellen Sie einfach eine Befehlsliste als Zeichnungs Ziel des aktuellen Geräte Kontexts und legen Sie dann auf diesen Gerätekontext fest, genau so, als ob Sie auf ein bitmapziel für die Anzeige zeichnen. Weitere Informationen zu Geräten und Zielen finden Sie unter [Geräte und Geräte Kontexte](devices-and-device-contexts.md) .

Das Diagramm zeigt die Interaktion zwischen der APP, dem Gerätekontext, dem bitmapziel, dem Ziel der Befehlsliste und dem Druck Steuerelement.

> [!Note]  
> Die Druck Sub-System und Drucker Komponenten von Windows sind grau, da Sie in [Direct2D](./direct2d-portal.md) -apps vollständig ausgeblendet sind.

![ein Diagramm, das zeigt, wie die CommandList und der Druckvorgang mit einer APP und Direct2D interagieren.](images/d2dprintcontroldiagram.png)

## <a name="example"></a>Beispiel

Der gesamte Druck Direct2D Inhalt umfasst die folgenden Schritte.

1.  Erstellen Sie ein Druck Steuerelement zum Initiieren eines Druckauftrags.
2.  Fügen Sie dem Druck Steuerelement eine Seite hinzu, indem Sie eine Befehlsliste übergeben.
3.  Wiederholen Sie Schritt 2 für jede Seite im restlichen Dokument.
4.  Schließen Sie das Druck Steuerelement, um den Druckauftrag abzuschließen.

Hier sehen Sie ein Codebeispiel, in dem der Prozess veranschaulicht wird.

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a>Zugehörige Themen

[**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[Verbessern der Leistung von Direct2D-Anwendungen und Drucken](improving-direct2d-performance.md)