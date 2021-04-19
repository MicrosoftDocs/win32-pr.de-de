---
description: Die cbaserendererinputpin-Klasse implementiert eine Eingabe-PIN für die cbasererererklasse. Sofern nicht angegeben, werden die Methoden in dieser Klasse an die entsprechenden Methoden der cbasererererklasse delegiert.
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: Crendererinputpin-Klasse (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ec48b31170b2233f211e7e72de81d8792ae9160
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358786"
---
# <a name="crendererinputpin-class"></a>Crendererinputpin-Klasse

![crendererinput-Pin-Klassenhierarchie](images/rbase01.png)

Die **cbaserendererinputpin** -Klasse implementiert eine Eingabe-PIN für die [**cbasererererklasse**](cbaserenderer.md) . Sofern nicht angegeben, werden die Methoden in dieser Klasse an die entsprechenden Methoden der **cbasererererklasse** delegiert.



| Geschützte Member-Variablen                                       | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m- \_ prenderer**](crendererinputpin-m-prenderer.md)            | Zeiger auf den Filter.                                                                 |
| Öffentliche Methoden                                                   | BESCHREIBUNG                                                                            |
| [**Crendererinputpin**](crendererinputpin-crendererinputpin.md) | Konstruktormethode.                                                                    |
| [**Breakconnect**](crendererinputpin-breakconnect.md)           | Fügt beim Abbrechen einer Verbindung angepassten Code hinzu.                                       |
| [**Completeconnect**](crendererinputpin-completeconnect.md)     | Schließt die Verbindung ab.                                                              |
| [**Checkmediatype**](crendererinputpin-checkmediatype.md)       | Bestimmt, ob die PIN einen bestimmten Medientyp unterstützen kann.                               |
| [**Aktiv**](crendererinputpin-active.md)                       | Schaltet die PIN in den aktiven (angehaltenen oder laufenden) Modus.                               |
| [**Inaktiv**](crendererinputpin-inactive.md)                   | Schaltet die PIN in einen inaktiven Zustand und gibt den Speicher der Zuweisung frei.        |
| [**Setmediatype**](crendererinputpin-setmediatype.md)           | Legt den Medientyp der PIN fest.                                                        |
| [**Allocator**](crendererinputpin-allocator.md)                 | Ruft einen Zeiger auf die Standard Speicherzuweisung ab.                                   |
| IPin-Methoden                                                     | BESCHREIBUNG                                                                            |
| [**QueryId**](crendererinputpin-queryid.md)                     | Ruft einen Bezeichner für die PIN ab.                                                   |
| [**EndOfStream**](crendererinputpin-endofstream.md)             | Teilt der PIN mit, dass keine weiteren Daten erwartet werden, bis ein neuer Befehl zum Ausführen ausgegeben wird. |
| [**Beginflush**](crendererinputpin-beginflush.md)               | Teilt der PIN mit, einen Leerungs Vorgang zu starten.                                            |
| [**Endflush**](crendererinputpin-endflush.md)                   | Teilt der PIN mit, einen Leerungs Vorgang zu beenden.                                              |
| IMemInputPin-Methoden                                             | BESCHREIBUNG                                                                            |
| [**Medizinisch**](crendererinputpin-receive.md)                     | Ruft den nächsten Datenblock aus dem Stream ab.                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




