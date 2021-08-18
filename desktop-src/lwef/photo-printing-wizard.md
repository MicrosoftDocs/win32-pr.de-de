---
title: Fotodruck-Assistent
description: Der Fotodruck-Assistent unterstützt Benutzer beim Drucken von Fotos, indem er eine benutzerfreundliche Benutzeroberfläche des Assistenten bereitstellt.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Fotodruck-Assistent
- IDropTarget, Fotodruck-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38199f7977e428f41cbc0560e0eab9ad2e106709579255ec8c3a1e74d7f7a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475447"
---
# <a name="photo-printing-wizard"></a>Fotodruck-Assistent

Der Fotodruck-Assistent unterstützt Benutzer beim Drucken von Fotos, indem er eine benutzerfreundliche Benutzeroberfläche des Assistenten bereitstellt. Der Assistent ermöglicht es dem Benutzer, Fotodruckgrößen und andere Druckoptionen anzugeben, und sendet die Fotos dann an den Drucker. Der Assistent ist so konzipiert, dass er programmgesteuert von jeder Anwendung aufgerufen werden kann, die Benutzern die Möglichkeit bieten möchte, Fotos zu drucken und Größen- und andere Druckoptionen anzugeben. Der Fotodruck-Assistent ist auf Windows XP und Windows Vista verfügbar.

-   [Vom Fotodruck-Assistenten bereitgestellte Funktionen](#features-provided-by-the-photo-print-wizard)
-   [Unterstützte Fotodateiformate](#supported-photo-file-formats)
-   [Programmgesteuertes Starten des Fotodruck-Assistenten](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a>Vom Fotodruck-Assistenten bereitgestellte Funktionen

Der Fotodruck-Assistent bietet mehrere Optionen, die in gängigen Druckerdialogfeldern möglicherweise nicht verfügbar sind, z. B. Vorlagen mit mehreren Layouts mit genauen Abmessungen. Mithilfe der Layoutvorlagen können Benutzer den verfügbaren Platz auf Papierdruck am effizientesten nutzen. Weitere Optionen, die über den Fotodruck-Assistenten angegeben oder aufgerufen werden können, sind:

-   Auswählen eines Druckers aus einer Liste verfügbarer Drucker oder virtueller Druckziele (z. B. Microsoft XPS Document Writer). Auf Windows Vista sind abhängig von den Funktionen des Druckers oder des virtuellen Druckziels möglicherweise die folgenden Optionen verfügbar:
    -   Papiergröße. Beispiel: "Letter", "Legal", "A3".
    -   Druckqualität in Bezug auf unterstützte Auflösungen von DPI-Auflösungen (Dots per Inch).
    -   Papiertyp. Beispiel: "Plain" oder "Plainy".
-   Starten der Druckeinstellungen und -eigenschaften für einen bestimmten Drucker.
-   Festlegen **der Bildkopien** (auf Windows Vista) oder **Anzahl der Verwendeten bilder** (auf Windows XP) Drehfeldwerte.
-   Angeben einer Drucklayoutvorlage. Beispiel: **Vollständiges Seitenfoto** oder **Wallet gibt aus.**
-   Auswählen der Option **Bild an Frame anpassen** (nur auf Windows Vista verfügbar).
-   Anzeigen einer Vorschau des gedruckten Fotos mit den derzeit angegebenen Optionen.
-   Zugriff auf erweiterte Druckoptionen, z. **B. Sharpen für Druck** und **Farbverwaltung** (nur auf Windows Vista verfügbar).

Jede Anwendung kann von den Funktionen und der Fotodruckfunktion des Fotodruck-Assistenten profitieren. Eine Anwendung kann die dateien übergeben, die gedruckt werden sollen. Der Fotodruck-Assistent übernimmt dann die Vorbereitung der Datei für den Druck basierend auf den vom Benutzer angegebenen Optionen und sendet die vorbereiteten Dateien an den Drucker.

Die folgende Abbildung zeigt die Benutzeroberfläche des Fotodruck-Assistenten auf Windows Vista.

![Der Fotodruck-Assistent unter Windows Vista](images/ppw-vista.png)

Die folgende Abbildung zeigt die Benutzeroberfläche des Fotodruck-Assistenten auf Windows XP.

![Der Fotodruck-Assistent unter Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a>Unterstützte Fotodateiformate

Auf Windows XP unterstützt der Fotodruck-Assistent alle Grafikdateiformate, die von Windows GDI+ unterstützt werden. Derzeit umfassen diese Dateiformate Folgendes:

-   Bitmap (BMP)
-   GIF (Graphics Interchange Format)
-   JPEG (Joint Photographic Experts Group)
-   Exchangeable Image File (EXIF)
-   PNG (Portable Network Graphics)
-   TIFF (Tagged Image File Format)

Weitere Informationen zu Grafikdateiformaten, die von GDI+ unterstützt werden, finden Sie unter [Bitmaptypen.](../gdiplus/-gdiplus-types-of-bitmaps-about.md)

Auf Windows Vista unterstützt der Fotodruck-Assistent jedes Bilddateiformat, für das ein WIC-Codec (Windows Imaging Component) installiert ist. WIC bietet mehrere Standardcodecs, einschließlich:

-   Bitmap (BMP)
-   GIF
-   Symbolformat (ICO)
-   JPEG
-   PNG
-   TIFF
-   Windows Medienfotoformat

Weitere Informationen zu WIC- und WIC-Codecs finden Sie unter [Windows Imaging-Komponente.](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)

## <a name="programmatically-launching-the-photo-print-wizard"></a>Programmgesteuertes Starten des Fotodruck-Assistenten

Um den Fotodruck-Assistenten aufzurufen, rufen Sie die [IDropTarget-Schnittstelle](/windows/win32/api/oleidl/nn-oleidl-idroptarget) mit dem folgenden Klassenbezeichner (CLSID) auf:


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



Die Dateien, die vom Fotodruck-Assistenten verarbeitet werden sollen, werden in einem [IDataObject-Objekt](/windows/win32/api/objidl/nn-objidl-idataobject) angegeben.

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



 

 