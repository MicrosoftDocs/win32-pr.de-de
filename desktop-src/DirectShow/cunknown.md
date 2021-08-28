---
description: Die CUnknown-Klasse implementiert die IUnknown-Schnittstelle. Die meisten Component Object Model -Objekte (COM) in DirectShow werden von CUnknown abgeleitet.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: CUnknown-Klasse (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06b6089f7f1c108a9b99ad4f1b16f4638b84d8d687a3590353c32841ccfff499
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075995"
---
# <a name="cunknown-class"></a>CUnknown-Klasse

![cunknown-Klassenhierarchie](images/cbase01.png)

Die **CUnknown-Klasse** implementiert die **IUnknown-Schnittstelle.** Die meisten Component Object Model -Objekte (COM) in DirectShow werden von **CUnknown** abgeleitet.

Wenn Sie ein COM-Objekt implementieren, sollten Sie es von **CUnknown** ableiten. Die Ableitung von **CUnknown** bietet eine threadsichere Implementierung und spart Ihnen das Implementieren von **IUnknown.**

Eine ausführliche Erläuterung der Verwendung dieser Basisklasse finden Sie unter [Implementieren von IUnknown.](how-to-implement-iunknown.md) Es folgt eine kurze Zusammenfassung:

-   Schließen Sie das [**DECLARE \_ IUNKNOWN-Makro**](declare-iunknown.md) in den öffentlichen Abschnitt Ihrer Klassendefinition ein. Dieses Makro deklariert die drei Methoden der **IUnknown-Schnittstelle.**
-   Überschreiben Sie die [**NonDelegatingQueryInterface-Methode,**](cunknown-nondelegatingqueryinterface.md) um andere Schnittstellen als **IUnknown** zu unterstützen. Rufen Sie innerhalb dieser Methode die [**GetInterface-Funktion**](getinterface.md) auf, um Schnittstellenzeiger abzurufen.
-   Rufen Sie in Ihrem Klassenkonstruktor die **CUnknown-Konstruktormethode** auf.



| Geschützte Membervariablen                                                  | BESCHREIBUNG                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**m \_ cRef**](cunknown-m-cref.md)                                          | Verweisanzahl.                                                   |
| Öffentliche Methoden                                                              | BESCHREIBUNG                                                        |
| [**CUnknown**](cunknown-cunknown.md)                                       | Konstruktormethode.                                                |
| [**~ CUnknown**](cunknown--cunknown.md)                                    | Destruktormethode. Virtuellen.                                        |
| [**GetOwner**](cunknown-getowner.md)                                       | Ruft einen Zeiger auf die steuernde **IUnknown** ab.                    |
| INonDelegatingUnknown-Methoden                                               | BESCHREIBUNG                                                        |
| [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md)                 | Erhöht den Verweiszähler.                                    |
| [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) | Ruft einen Schnittstellenzeiger ab und erhöht den Verweiszähler. |
| [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md)               | Dekrement wird der Verweiszähler.                                    |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 




