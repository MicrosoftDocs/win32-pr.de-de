---
description: Die CImagePalette-Klasse verwaltet Paletten für Videorenderer. Sie kann verwendet werden, um eine logische Palette aus einem Videoformat zu erstellen. Diese Klasse ist für die Verwendung mit den Klassen CBaseWindow und CDrawImage vorgesehen, sodass sie etwas spezialisiert ist.
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: CImagePalette-Klasse
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
ms.openlocfilehash: 390bd4fc60e7d20264ae3a9238699108e7778524b73c6af22038197260da4463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074064"
---
# <a name="cimagepalette-class"></a>CImagePalette-Klasse

Die `CImagePalette` -Klasse verwaltet Paletten für Videorenderer. Sie kann verwendet werden, um eine logische Palette aus einem Videoformat zu erstellen. Diese Klasse ist für die Verwendung mit den [**Klassen CBaseWindow**](cbasewindow.md) und [**CDrawImage**](cdrawimage.md) vorgesehen, sodass sie etwas spezialisiert ist.



| Geschützte Membervariablen                                       | Beschreibung                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ hPalette**](cimagepalette-m-hpalette.md)                  | Handle für die logische Palette, die von diesem Objekt verwaltet wird.                                        |
| [**m \_ pBaseWindow**](cimagepalette-m-pbasewindow.md)            | Zeiger auf das **CBaseWindow-Objekt,** das das Fenster verwaltet.                                 |
| [**m \_ pDrawImage**](cimagepalette-m-pdrawimage.md)              | Zeiger auf das **CDrawImage-Objekt,** das das Videobild zeichnet.                               |
| [**m \_ pFilter**](cimagepalette-m-pfilter.md)                    | Zeiger auf den besitzenden Filter.                                                                  |
| Öffentliche Methoden                                                   | Beschreibung                                                                                    |
| [**CImagePalette**](cimagepalette-cimagepalette.md)             | Konstruktormethode.                                                                            |
| [**CopyPalette**](cimagepalette-copypalette.md)                 | Kopiert die Palette aus einer beliebigen **VIDEOINFO-Struktur** in eine beliebige palettierte **VIDEOINFO-Struktur.** |
| [**MakeIdentityPalette**](cimagepalette-makeidentitypalette.md) | Versucht, eine Palette zu erstellen, die direkt der im Anzeigegerät ausgewählten Palette zugeordnet wird.   |
| [**MakePalette**](cimagepalette-makepalette.md)                 | Erstellt eine logische Palette aus der Farbtabelle in einem Videoformat.                              |
| [**PreparePalette**](cimagepalette-preparepalette.md)           | Richtet eine Palette basierend auf einem Medientyp aus dem besitzenden Filter ein.                               |
| [**RemovePalette**](cimagepalette-removepalette.md)             | Löscht die vorhandene logische Palette.                                                          |



 

 

 



