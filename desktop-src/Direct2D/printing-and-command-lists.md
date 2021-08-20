---
title: Druck- und Befehlslisten
description: Das Steuerelement Direct2D \ 32;print ist eine neue Komponente im Direct2D-Modul in Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0026071ce8e78fc2ea946e0fffff2993e32ab48a2a20d4de6cdb12ca9b1eaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075048"
---
# <a name="printing-and-command-lists"></a>Druck- und Befehlslisten

Das [Direct2D-Drucksteuerelement](./direct2d-portal.md) [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) ist eine neue Komponente im Direct2D-Modul in Windows 8. Mit dieser Komponente können Direct2D-Apps ihre Direct2D-Zeichnungsaufrufe wiederverwenden (in Bezug auf Zustandsänderungen und Zurückungsprimitiven), um Druckergebnisse zu liefern, die denen auf dem Bildschirm ähneln.

Die [**ID2D1PrintControl-Schnittstelle**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) stellt einen virtuellen Druckauftrag dar: Sie können ein [Direct2D-Drucksteuer](./direct2d-portal.md) steuerelement erstellen, um einen neuen Druckauftrag zu initiieren, Direct2D-Inhalt für jede Seite übergeben, die Sie drucken möchten, und dann das Drucksteuerblatt schließen, um einen Druckauftrag zu abschließen.

> [!Note]  
> Ein Drucksteuer steuerelement wird einem und genau einem Druckauftrag zuordnungen, und Sie können es nicht wiederverwenden.

Das [Direct2D-Drucksteuer](./direct2d-portal.md) steuerelement konvertiert und optimiert den übergebenen Direct2D-Inhalt für das Druckuntersystem, das mit den echten Druckern arbeitet, um den tatsächlichen Druck zu liefern. Alle druckspezifischen Details werden in Direct2D-Apps ausgeblendet. Dies bedeutet, dass Direct2D-Apps drucken können, ohne zu wissen, auf welche Geräte sie zeichnen oder wie die Zeichnungen in den Druck übersetzt werden.

Zum Drucken mit [Direct2D](./direct2d-portal.md)müssen Sie eine Direct2D-Befehlsliste für jede Seite vorbereiten, die Sie drucken möchten, und diese Befehlsliste dann an das Direct2D-Drucksteuersystem übergeben. Um diese Direct2D-Befehlsliste vorzubereiten, erstellen und legen Sie einfach eine Befehlsliste als Zeichnungsziel des aktuellen Gerätekontexts fest und zeichnen dann in diesen Gerätekontext, genau so, als würden Sie auf ein Bitmapziel für die Anzeige zeichnen. Weitere [Informationen zu Geräten und](devices-and-device-contexts.md) Zielen finden Sie unter Geräte und Gerätekontexte.

Das Diagramm hier veranschaulicht die Interaktion zwischen der App, dem Gerätekontext, dem Bitmapziel, dem Befehlslistenziel und dem Drucksteuergerät.

> [!Note]  
> Die Windows Print Sub-System- und Printer-Komponenten sind grau, da sie vollständig für [Direct2D-Apps ausgeblendet](./direct2d-portal.md) sind.

![Ein Diagramm, das zeigt, wie die Befehlsliste und das Drucken mit einer App und direct2d interagieren.](images/d2dprintcontroldiagram.png)

## <a name="example"></a>Beispiel

Der vollständige Prozess zum Drucken von Direct2D-Inhalten umfasst die folgenden Schritte.

1.  Erstellen Sie ein Drucksteuer steuerelement, um einen Druckauftrag zu initiieren.
2.  Fügen Sie dem Drucksteuer steuerelement eine Seite hinzu, indem Sie eine Befehlsliste übergeben.
3.  Wiederholen Sie Schritt 2 für jede Seite im restlichen Dokument.
4.  Schließen Sie das Drucksteuer steuerelement, um den Druckauftrag fertig zu stellen.

Hier sehen Sie ein Codebeispiel, das den Prozess zeigt.

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