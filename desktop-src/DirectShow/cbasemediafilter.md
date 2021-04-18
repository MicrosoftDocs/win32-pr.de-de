---
description: Die cbasemediafilter-Klasse implementiert die imediafilter-Schnittstelle.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: Cbasemediafilter-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e594fd941fffecc836af26bd3d70cced82ddcaa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357611"
---
# <a name="cbasemediafilter-class"></a>Cbasemediafilter-Klasse

![cbasemediafilter](images/filter05.png)

Die- `CBaseMediaFilter` Klasse implementiert die [**imediafilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) -Schnittstelle. Verwenden Sie diese Klasse für Plug-in-Verteiler oder andere Objekte, die **imediafilter** unterstützen müssen, ohne die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle zu unterstützen. Verwenden Sie diese Klasse nicht für Filter. Verwenden Sie stattdessen die [**cbasefilter**](cbasefilter.md) -Klasse oder eine Basisklasse, die von **cbasefilter** abgeleitet ist.



| Geschützte Member-Variablen                                       | BESCHREIBUNG                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [**m- \_ Status**](cbasemediafilter-m-state.md)                     | Aktueller Status des Objekts.                                 |
| [**m \_ pclock**](cbasemediafilter-m-pclock.md)                   | Zeiger auf die verweisuhr des Objekts.                     |
| [**m \_ tSTART**](cbasemediafilter-m-tstart.md)                   | Die Verweis Zeit, die der streamzeit 0 entspricht.            |
| [**m \_ CLSID**](cbasemediafilter-m-clsid.md)                     | Klassen Bezeichner (CLSID) des Objekts.                      |
| [**m \_ Plock**](cbasemediafilter-m-plock.md)                     | Zeiger auf einen kritischen Abschnitt.                               |
| Öffentliche Methoden                                                   | BESCHREIBUNG                                                  |
| [**Cbasemediafilter**](cbasemediafilter-cbasemediafilter.md)    | Konstruktormethode.                                          |
| [**~ Cbasemediafilter**](cbasemediafilter--cbasemediafilter.md) | Dekonstruktormethode. Virtu.                                  |
| [**Streamtime**](cbasemediafilter-streamtime.md)                | Ruft die aktuelle streamzeit ab. Virtu.                  |
| [**IsActive**](cbasemediafilter-isactive.md)                    | Bestimmt, ob das Objekt aktiv ist (wird ausgeführt oder angehalten). |
| Ipersistent-Methoden                                                 | BESCHREIBUNG                                                  |
| [**GetClassID**](cbasemediafilter-getclassid.md)                | Ruft den Klassen Bezeichner ab.                              |
| Imediafilter-Methoden                                             | BESCHREIBUNG                                                  |
| [**GetState**](cbasemediafilter-getstate.md)                    | Ruft den Status des Objekts ab (wird ausgeführt, beendet oder angehalten).  |
| [**Setsyncsource**](cbasemediafilter-setsyncsource.md)          | Legt eine Referenzuhr für das-Objekt fest.                       |
| [**Getsyncsource**](cbasemediafilter-getsyncsource.md)          | Ruft die vom-Objekt verwendete Referenzuhr ab.      |
| [**Stop**](cbasemediafilter-stop.md)                            | Beendet das-Objekt.                                            |
| [**Anhalten**](cbasemediafilter-pause.md)                          | Hält das-Objekt an.                                           |
| [**Ausführen**](cbasemediafilter-run.md)                              | Führt das-Objekt aus.                                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




