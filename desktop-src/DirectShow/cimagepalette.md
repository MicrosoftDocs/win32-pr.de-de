---
description: Die cimagepalette-Klasse verwaltet Paletten für Videorenderer. Sie kann verwendet werden, um eine logische Palette aus einem Videoformat zu erstellen. Diese Klasse ist für die Verwendung mit den cbasewindow-und cdrawimage-Klassen vorgesehen, sodass Sie etwas spezieller ist.
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: Cimagepalette-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette
api_type:
- COM
api_location: ''
ms.openlocfilehash: 696c51e4918815e18accbadd66c764493dc0b98e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346386"
---
# <a name="cimagepalette-class"></a>Cimagepalette-Klasse

Die- `CImagePalette` Klasse verwaltet Paletten für Videorenderer. Sie kann verwendet werden, um eine logische Palette aus einem Videoformat zu erstellen. Diese Klasse ist für die Verwendung mit den [**cbasewindow**](cbasewindow.md) -und [**cdrawimage**](cdrawimage.md) -Klassen vorgesehen, sodass Sie etwas spezieller ist.



| Geschützte Member-Variablen                                       | BESCHREIBUNG                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ hpalette**](cimagepalette-m-hpalette.md)                  | Handle für die logische Palette, die von diesem Objekt verwaltet wird.                                        |
| [**m \_ pbasewindow**](cimagepalette-m-pbasewindow.md)            | Zeiger auf das **cbasewindow** -Objekt, das das Fenster verwaltet.                                 |
| [**m \_ pdrawimage**](cimagepalette-m-pdrawimage.md)              | Zeiger auf das **cdrawimage** -Objekt, das das Videobild zeichnet.                               |
| [**m \_ pFilter**](cimagepalette-m-pfilter.md)                    | Zeiger auf den besitzenden Filter.                                                                  |
| Öffentliche Methoden                                                   | BESCHREIBUNG                                                                                    |
| [**Cimagepalette**](cimagepalette-cimagepalette.md)             | Konstruktormethode.                                                                            |
| [**CopyPalette**](cimagepalette-copypalette.md)                 | Kopiert die Palette aus einer beliebigen **videoinfo** -Struktur in eine beliebige paletsierte **videoinfo** -Struktur. |
| [**Makeidentitypalette**](cimagepalette-makeidentitypalette.md) | Versucht, eine Palette zu erstellen, die direkt der im Anzeigegerät ausgewählten Palette zugeordnet wird.   |
| [**Makepalette**](cimagepalette-makepalette.md)                 | Erstellt eine logische Palette aus der Farbtabelle in einem Videoformat.                              |
| [**PreparePalette**](cimagepalette-preparepalette.md)           | Richtet eine Palette auf der Grundlage eines Medientyps aus dem besitzenden Filter ein.                               |
| [**RemovePalette**](cimagepalette-removepalette.md)             | Löscht die vorhandene logische Palette.                                                          |



 

 

 



