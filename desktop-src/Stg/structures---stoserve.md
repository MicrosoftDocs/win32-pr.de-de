---
title: Strukturen-stoservice
description: Copaper verpackt die Stift Farbe, die Breite und die Koordinaten in inkdata-Strukturen und speichert Sie in einem dynamisch zugeordneten Array, das im Arbeitsspeicher verwaltet wird.
ms.assetid: 25e68c39-5306-4ad6-85dd-a8a5e256abf0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9868f38d7915185b8d3511bd1bf6faa9c7a1e1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947616"
---
# <a name="structures---stoserve"></a>Strukturen-stoservice

Copaper verpackt die Stift Farbe, die Breite und die Koordinaten in **inkdata** -Strukturen und speichert Sie in einem dynamisch zugeordneten Array, das im Arbeitsspeicher verwaltet wird.

## <a name="inkdata-structure"></a>Inkdata-Struktur

Im folgenden finden Sie die Deklarationen für die **inkdata** -Struktur aus "Paper. H".

``` syntax
// The types of Ink Data.
#define INKTYPE_NONE  0
#define INKTYPE_START 1
#define INKTYPE_DRAW  2
#define INKTYPE_STOP  3

  // The Ink Data structure.
  typedef struct _INKDATA
  {
    SHORT nType;            // Ink Type.
    SHORT nX;               // X-coordinate of ink point.
    SHORT nY;               // Y-coordinate of ink point.
    SHORT nWidth;           // Ink line width in pixels.
    COLORREF crColor;       // Ink color.
  } INKDATA;
```

Auf das dynamische Array dieser **inkdata** -Pakete wird durch m \_ painkdata, ein Member der [**iPaper**](ipaper-methods.md) -Implementierungs Klasse, verwiesen. Das Array wird in der **iPaper:: initpaper** -Methode mit einer anfänglichen Zuordnung erstellt. Weitere Informationen finden Sie in der **initpaper** -Methode und in der privaten nextlot-hilfsprogrammmethode der cimpipaper-Implementierung in Paper. H. Die [**inkstart**](inkstart-method.md)-, [**inkdraw**](inkdraw-method.md)-und [**inkstoppt**](cguipaper-methods.md) -Methoden verwenden nextslot, um neue Slots im Array abzurufen. Das Array wird nach Bedarf dynamisch erweitert.

Der Client ruft die [**iPaper:: Erase**](ipaper-methods.md) -Methode auf, um die aktuelle Zeichnung zu löschen. Diese Methode weist das Array nicht neu zu. Es werden einfach alle aktuellen frei Hand Daten als inktype \_ None gekennzeichnet und der Dateiende-Index des Arrays auf Null zurückgesetzt.

Der Client ruft die [**iPaper:: Lock**](ipaper-methods.md) -Methode und die **Unlock** -Methode auf, um den Besitz des copaper zum Zeichnen zu verwalten. Diese Methoden werden bereitgestellt, um den Zugriff auf mehrere Clients auf die Zeichnung zu organisieren, die in einem freigegebenen copaper aufbewahrt wird.

## <a name="paper_properties-structure"></a>Struktur der Papier \_ Eigenschaften

Der Client ruft die [**iPaper:: Resize**](ipaper-methods.md) -Methode auf, um copaper mitzuteilen, dass der Benutzer die Größe des aktuellen Zeichnungs Papier Rechtecks geändert hat. Diese Koordinatendaten werden in einer **Papier \_ Eigenschafts** Struktur aufbewahrt, die mit den frei Hand Daten gespeichert wird, wenn alle Papier Daten in einer Verbund Datei gespeichert werden.

Im folgenden finden Sie die Deklaration der **Papier \_ Eigenschaften** aus Paper. H.

``` syntax
#define PAPER_TITLE_SIZE 64
  typedef struct _PAPER_PROPERTIES
  {
    LONG lInkDataVersion;
    LONG lInkArraySize;
    COLORREF crWinColor;
    RECT WinRect;
    WCHAR wszTitle[PAPER_TITLE_SIZE];
    WCHAR wszAuthor[PAPER_TITLE_SIZE];
    WCHAR wszReserved1[PAPER_TITLE_SIZE];
    WCHAR wszReserved2[PAPER_TITLE_SIZE];
  } PAPER_PROPERTIES;
```

Die Struktur der **Papier \_ Eigenschaften** ist so konzipiert, dass jederzeit neue frei Hand Datenformate hinzugefügt werden können, wenn die Komponente dllpaper weiterentwickelt wird. Die [**iPaper**](ipaper-methods.md) -Schnittstelle ist allgemein genug, dass eine nachfolgende Version der dllpaper-Komponente ein anderes frei Hand Datenformat speichern kann, während dieselbe **iPaper** -Schnittstelle implementiert wird. Da die Methoden von **iPaper** nicht von einem bestimmten Freihand-Datenformat abhängen, kann eine neue Version der dllpaper-Komponente, die ein anderes frei Hand Datenformat unterstützt, dieselbe Schnittstelle verwenden.

Die in einer Verbund Datei gespeicherten Papiereigenschaften zeichnen die aktuelle Größe des frei Hand Daten Arrays auf. Die richtige Array Größe kann dann zugewiesen werden, um die aus der Datei gelesenen frei Hand Daten zu unterstützen.

In der Struktur der **Papier \_ Eigenschaften** werden auch die Zeichnungs Rechtecke-Größe und Hintergrund Fenster Farbe der Papieroberfläche gespeichert.

Obwohl Sie nicht in den **stoservice** / -Beispielen von **stoservice** verwendet werden, können auch ein Zeichnungs Titel und ein Autorenname gespeichert werden.

Erstellungsdatum und Datum der letzten Änderung sind nicht in diesen Papiereigenschaften enthalten, da die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle, die für den Zugriff auf Verbund Dateien verwendet wird, diese Informationen verwaltet.

 

 




