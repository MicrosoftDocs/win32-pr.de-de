---
description: Die CBaseMediaFilter-Klasse implementiert die IMediaFilter-Schnittstelle.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: CBaseMediaFilter-Klasse (Amfilter.h)
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
ms.openlocfilehash: 16225ca289597bd8145e689912fd458a4f29d8aa4cc5ca68d6c3e0d0e3605ccc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586104"
---
# <a name="cbasemediafilter-class"></a>CBaseMediaFilter-Klasse

![cbasemediafilter](images/filter05.png)

Die `CBaseMediaFilter` -Klasse implementiert die [**IMediaFilter-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) Verwenden Sie diese Klasse für Plug-In-Verteiler oder andere Objekte, die **IMediaFilter** unterstützen müssen, ohne die [**IBaseFilter-Schnittstelle zu**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) unterstützen. Verwenden Sie diese Klasse nicht für Filter. Verwenden Sie stattdessen die [**CBaseFilter-Klasse**](cbasefilter.md) oder eine von **CBaseFilter abgeleitete Basisklasse.**



| Geschützte Membervariablen                                       | Beschreibung                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [**\_m-Status**](cbasemediafilter-m-state.md)                     | Aktueller Status des Objekts.                                 |
| [**m \_ pClock**](cbasemediafilter-m-pclock.md)                   | Zeiger auf die Referenzuhr des Objekts.                     |
| [**m \_ tStart**](cbasemediafilter-m-tstart.md)                   | Verweiszeit, die der Streamzeit 0 entspricht.            |
| [**m \_ clsid**](cbasemediafilter-m-clsid.md)                     | Klassenbezeichner (CLSID) des Objekts.                      |
| [**m \_ pLock**](cbasemediafilter-m-plock.md)                     | Zeiger auf einen kritischen Abschnitt.                               |
| Öffentliche Methoden                                                   | Beschreibung                                                  |
| [**CBaseMediaFilter**](cbasemediafilter-cbasemediafilter.md)    | Konstruktormethode.                                          |
| [**~ CBaseMediaFilter**](cbasemediafilter--cbasemediafilter.md) | Destruktormethode. Virtuellen.                                  |
| [**StreamTime**](cbasemediafilter-streamtime.md)                | Ruft die aktuelle Streamzeit ab. Virtuellen.                  |
| [**IsActive**](cbasemediafilter-isactive.md)                    | Bestimmt, ob das Objekt aktiv ist (wird ausgeführt oder angehalten). |
| IPersist-Methoden                                                 | Beschreibung                                                  |
| [**Getclassid**](cbasemediafilter-getclassid.md)                | Ruft den Klassenbezeichner ab.                              |
| IMediaFilter-Methoden                                             | Beschreibung                                                  |
| [**GetState**](cbasemediafilter-getstate.md)                    | Ruft den Zustand des Objekts ab (wird ausgeführt, beendet oder angehalten).  |
| [**SetSyncSource**](cbasemediafilter-setsyncsource.md)          | Legt eine Verweisuhr für das -Objekt fest.                       |
| [**GetSyncSource**](cbasemediafilter-getsyncsource.md)          | Ruft die Referenzuhr ab, die das -Objekt verwendet.      |
| [**Stoppen**](cbasemediafilter-stop.md)                            | Beendet das -Objekt.                                            |
| [**Anhalten**](cbasemediafilter-pause.md)                          | Hält das -Objekt an.                                           |
| [**Ausführung**](cbasemediafilter-run.md)                              | Führt das -Objekt aus.                                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




