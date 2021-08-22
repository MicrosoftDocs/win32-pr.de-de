---
title: Strukturen – StoServe
description: COPaper packt die Stiftfarbe, Breite und Koordinaten in INKDATA-Strukturen und speichert sie in einem dynamisch zugeordneten Array, das im Arbeitsspeicher verwaltet wird.
ms.assetid: 25e68c39-5306-4ad6-85dd-a8a5e256abf0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f81b46f2f0a992f27ed405361734fe53db98cf9272697b88866451ef1d7d4b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796890"
---
# <a name="structures---stoserve"></a>Strukturen – StoServe

COPaper packt die Stiftfarbe, Breite und Koordinaten in **INKDATA-Strukturen** und speichert sie in einem dynamisch zugeordneten Array, das im Arbeitsspeicher verwaltet wird.

## <a name="inkdata-structure"></a>INKDATA-Struktur

Im Folgenden finden Sie die Deklarationen für die **INKDATA-Struktur** von PAPER.H.

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

Auf das dynamische Array dieser **INKDATA-Pakete** verweist m paInkData, ein Member der \_ [**IPaper-Implementierungsklasse.**](ipaper-methods.md) Das Array wird in der **IPaper::InitPaper-Methode** mit einer anfänglichen Zuordnung erstellt. Weitere Informationen finden Sie unter **der InitPaper-Methode** und der privaten NextSlot-Hilfsprogrammmethode der CImpIPaper-Implementierung in PAPER.H. Die [**Methoden InkStart,**](inkstart-method.md) [**InkDraw**](inkdraw-method.md)und [**InkStop**](cguipaper-methods.md) verwenden NextSlot, um neue Slots im Array zu erhalten. Das Array wird bei Bedarf dynamisch durch NextSlot erweitert.

Der Client ruft die [**IPaper::Erase-Methode auf,**](ipaper-methods.md) um die aktuelle Zeichnung zu löschen. Mit dieser Methode wird das Array nicht neu zugewiesen. Es markiert einfach alle aktuellen Ink-Daten als INKTYPE NONE und setzt den \_ End-of-Data-Index des Arrays auf 0 (null) zurück.

Der Client ruft die [**IPaper::Lock- und Unlock-Methoden**](ipaper-methods.md) **auf,** um den Besitz von COPaper für das Zeichnen zu verwalten. Diese Methoden werden bereitgestellt, um den Zugriff auf die Zeichnung in einem freigegebenen COPaper zwischen mehreren Clients zu organisieren.

## <a name="paper_properties-structure"></a>PAPER \_ PROPERTIES-Struktur

Der Client ruft die [**IPaper::Resize-Methode**](ipaper-methods.md) auf, um COPaper zu informieren, dass der Benutzer die Größe des aktuellen Zeichnungsdokumentrechtecks geändert hat. Diese Koordinatendaten werden in einer **PAPER \_ PROPERTIES-Struktur** gespeichert, die mit den Ink-Daten gespeichert wird, wenn alle Papierdaten in einer Verbunddatei gespeichert werden.

Im Folgenden finden Sie die **PAPER \_ PROPERTIES-Deklaration** von PAPER.H.

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

Die **PAPER \_ PROPERTIES-Struktur** ist so konzipiert, dass jederzeit neue Ink-Datenformate hinzugefügt werden können, wenn die DllPaper-Komponente weiterentwickelt wird. Die [**IPaper-Schnittstelle**](ipaper-methods.md) ist so allgemein, dass eine nachfolgende Version der DllPaper-Komponente ein anderes Ink-Datenformat speichern kann, während die gleiche **IPaper-Schnittstelle implementiert** wird. Da die Methoden von **IPaper** nicht von einem bestimmten Ink-Datenformat abhängen, kann eine neue Version der DllPaper-Komponente, die ein anderes Ink-Datenformat unterstützt, dieselbe Schnittstelle verwenden.

Die in einer Verbunddatei gespeicherten Papiereigenschaften zeichnen die aktuelle Größe des Ink-Datenarrays auf. Die richtige Arraygröße kann dann zugeordnet werden, um die aus der Datei gelesenen Ink-Daten zu verarbeiten.

In **der \_ PAPER PROPERTIES-Struktur** werden auch die Zeichnungsrechteckgröße und die Hintergrundfensterfarbe der Papieroberfläche gespeichert.

Obwohl in den **StoServe** / **StoClien-Beispielen** nicht verwendet, können auch ein Zeichnungstitel und ein Autorenname gespeichert werden.

Erstellungsdatum und Datum der letzten Änderung sind in diesen Papiereigenschaften nicht enthalten, da diese Informationen von der [**IStorage-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-istorage) verwaltet werden, die für den Zugriff auf Verbunddateien verwendet wird.

 

 




