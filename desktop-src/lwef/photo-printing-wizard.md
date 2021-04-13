---
title: Fotodruck-Assistent
description: Der Fotodruck-Assistent unterstützt Benutzer beim Drucken von Fotos, indem er eine benutzerfreundliche Assistenten Schnittstelle bereitstellt.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Fotodruck-Assistent
- IDropTarget, Fotodruck-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708f051f658739cebd08e4f8643e5dd7fc0c6f7f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390293"
---
# <a name="photo-printing-wizard"></a>Fotodruck-Assistent

Der Fotodruck-Assistent unterstützt Benutzer beim Drucken von Fotos, indem er eine benutzerfreundliche Assistenten Schnittstelle bereitstellt. Der Assistent ermöglicht dem Benutzer die Angabe von Foto Druckgrößen und anderen Druckoptionen und sendet die Fotos dann an den Drucker. Der Assistent ist so konzipiert, dass er Programm gesteuert von jeder Anwendung aufgerufen werden kann, die Benutzern die Möglichkeit bietet, Fotos zu drucken und Größen und andere Druckoptionen anzugeben. Der Fotodruck-Assistent ist unter Windows XP und Windows Vista verfügbar.

-   [Vom Photo Print-Assistenten bereitgestellte Funktionen](#features-provided-by-the-photo-print-wizard)
-   [Unterstützte Foto Dateiformate](#supported-photo-file-formats)
-   [Programm gesteuertes Starten des Foto Druck-Assistenten](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a>Vom Photo Print-Assistenten bereitgestellte Funktionen

Der Fotodruck-Assistent bietet mehrere Optionen, die möglicherweise nicht in allgemeinen Drucker Dialogfeldern verfügbar sind, wie z. b. Vorlagen mit mehreren Layouts mit exakten Dimensionen. Mithilfe der Layoutvorlagen können Benutzer den im Papier Druck Papier verfügbaren Speicherplatz optimal nutzen. Weitere Optionen, die über den Foto Druck-Assistenten angegeben oder darauf zugegriffen werden können, sind:

-   Auswählen eines Druckers aus einer Liste der verfügbaren Drucker oder virtuellen Druck Ziele (z. b. Microsoft XPS Document Writer). Unter Windows Vista sind möglicherweise die folgenden Optionen verfügbar, abhängig von den Funktionen des Druckers oder des virtuellen Druck Ziels:
    -   Papierformat. Beispiel: "Letter", "Legal", "a3".
    -   Druckqualität in Bezug auf die unterstützten dpi-Auflösungen (dpi pro Zoll).
    -   Papiertyp. Beispiel: "Plain" oder "Glossy".
-   Starten der Druckeinstellungen und-Eigenschaften für einen bestimmten Drucker.
-   Festlegen der **Kopien jedes Bilds** (unter Windows Vista) oder der Häufigkeit **, mit der die einzelnen Bild** -Drehfeld Werte (auf Windows XP) verwendet werden.
-   Angeben einer Drucklayoutvorlage. Beispielsweise druckt ein **vollständiges Foto** oder eine **Brieftasche**.
-   Auswählen der Option **Bild an Frame anpassen** (nur unter Windows Vista verfügbar).
-   Anzeigen einer Vorschau auf das gedruckte Foto mit den derzeit angegebenen Optionen.
-   Zugriffsmöglichkeiten für erweiterte Druckoptionen, z. b. **für die Druck** -und **Farbverwaltung** (nur unter Windows Vista verfügbar).

Jede Anwendung kann von den Funktionen und der Foto Druckfunktion profitieren, die der Fotodruck-Assistent anbietet. Eine Anwendung kann die zu druckenden Dateien übergeben. Der Fotodruck-Assistent kümmert sich um die Vorbereitung der Datei für den Druck basierend auf den vom Benutzer angegebenen Optionen und sendet die vorbereiteten Dateien an den Drucker.

In der folgenden Abbildung wird die Schnittstelle für den Foto Druck-Assistenten unter Windows Vista angezeigt

![der Foto Druck-Assistent unter Windows Vista](images/ppw-vista.png)

In der folgenden Abbildung wird die Schnittstelle für den Foto Druck-Assistenten unter Windows XP angezeigt

![der Foto Druck-Assistent unter Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a>Unterstützte Foto Dateiformate

Unter Windows XP unterstützt der Foto Druck-Assistent alle Grafikdatei Formate, die von Windows GDI+ unterstützt werden. Derzeit umfassen folgende Dateiformate:

-   Bitmap (BMP)
-   GIF (Graphics Interchange Format)
-   JPEG (Joint Photographic Experts Group)
-   Austauschbare Bilddatei (EXIF)
-   PNG (Portable Network Graphics)
-   TIFF (Tagged Image File Format)

Weitere Informationen zu Grafikdatei Formaten, die von GDI+ unterstützt werden, finden Sie unter [Typen von Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).

Unter Windows Vista unterstützt der Foto Druck-Assistent alle Bild Dateiformate, für die ein Windows Imaging Component (WIC)-Codec installiert ist. WIC bietet mehrere Standard-Codecs, einschließlich:

-   Bitmap (BMP)
-   GIF
-   Symbol Format (ICO)
-   JPEG
-   PNG
-   TIFF
-   Windows Media-Fotoformat

Weitere Informationen zu WIC-und WIC-Codecs finden Sie unter [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx) .

## <a name="programmatically-launching-the-photo-print-wizard"></a>Programm gesteuertes Starten des Foto Druck-Assistenten

Um den Fotodruck-Assistenten aufzurufen, rufen Sie die [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle mit der folgenden Klassen Kennung (CLSID) auf:


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



Die Dateien, die vom Fotodruck-Assistenten verarbeitet werden sollen, werden in einem [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) -Objekt angegeben.

Im folgenden Codebeispiel wird veranschaulicht, wie der Fotodruck-Assistent aufgerufen wird.


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
            
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PrintPhotosDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



 

 