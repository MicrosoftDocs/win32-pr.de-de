---
description: In diesem Thema werden die Konstruktoren der Region-Klasse aufgeführt. Eine vollständige Klassenauflistung finden Sie unter Region-Klasse.
ms.assetid: 94f4971c-defa-43e0-a0c0-4000557b0a5c
title: Region.Region-Konstruktoren
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: af5b5daf50a2e9487ddbf18450735a525f771717a94dc37ab20222c6c6fbe288
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115250"
---
# <a name="regionregion-constructors"></a>Region.Region-Konstruktoren

In diesem Thema werden die Konstruktoren der [**Region-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region) aufgeführt. Eine vollständige Klassenauflistung finden Sie unter **Region Class**.

### <a name="overload-list"></a>Überladeliste



| Konstruktor                                                                 | BESCHREIBUNG                                                                                                                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Region (HRGN)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inhrgn))                  | Erstellt eine Region, die mit der Region identisch ist, die von einem Handle für einen GDI-Bereich angegeben wird.<br/>                                                                                       |
| [**Region(Rect&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrect_))            | Erstellt einen Bereich, der durch ein Rechteck definiert wird.<br/>                                                                                                                                      |
| [**Region(RectF&)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstrectf_))          | Erstellt einen Bereich, der durch ein Rechteck definiert wird.<br/>                                                                                                                                      |
| [**Region(BYTE \* , INT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstbyte_inint)) | Erstellt einen Bereich, der durch Daten definiert wird, die aus einer anderen Region erhalten wurden. <br/>                                                                                                               |
| [**Region(GraphicsPath \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(inconstgraphicspath))        | Erstellt einen Bereich, der durch einen Pfad (ein [**GraphicsPath-Objekt)**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) definiert wird und über einen Füllmodus verfügt, der im **GraphicsPath-Objekt enthalten** ist.<br/> |
| [**Region()**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-region(constregion_))                           | Erstellt einen unendlichen Bereich. Dies ist der Standardkonstruktor <br/>                                                                                                                  |



 

 
