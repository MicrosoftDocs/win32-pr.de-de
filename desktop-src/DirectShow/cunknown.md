---
description: Die cunknown-Klasse implementiert die IUnknown-Schnittstelle. Die meisten Component Object Model (com)-Objekte in DirectShow werden von cunknown abgeleitet.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: Cunknown-Klasse (ComBase. h)
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
ms.openlocfilehash: 4818a088119f7cba25ce8a470f63cab722998c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354720"
---
# <a name="cunknown-class"></a>Cunknown-Klasse

![cunknown-Klassenhierarchie](images/cbase01.png)

Die **cunknown** -Klasse implementiert die **IUnknown** -Schnittstelle. Die meisten Component Object Model (com)-Objekte in DirectShow werden von **cunknown** abgeleitet.

Wenn Sie ein COM-Objekt implementieren, sollten Sie es ggf. von **cunknown** ableiten. Die Ableitung von **cunknown** bietet eine Thread sichere Implementierung und erspart Ihnen das Implementieren von **IUnknown**.

Ausführliche Informationen zur Verwendung dieser Basisklasse finden Sie unter Gewusst wie: [Implementieren von IUnknown](how-to-implement-iunknown.md). Im folgenden finden Sie eine kurze Zusammenfassung:

-   Fügen Sie das Makro [**Declare \_ IUnknown**](declare-iunknown.md) in den Abschnitt Public der Klassendefinition ein. Dieses Makro deklariert die drei Methoden der **IUnknown** -Schnittstelle.
-   Überschreiben Sie die [**nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) -Methode, um andere Schnittstellen als **IUnknown** zu unterstützen. Rufen Sie in dieser Methode die [**GetInterface**](getinterface.md) -Funktion zum Abrufen von Schnittstellen Zeigern auf.
-   Rufen Sie in Ihrem Klassenkonstruktor die **cunknown** -Konstruktormethode auf.



| Geschützte Member-Variablen                                                  | BESCHREIBUNG                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**m- \_ kref**](cunknown-m-cref.md)                                          | Verweis Zähler.                                                   |
| Öffentliche Methoden                                                              | BESCHREIBUNG                                                        |
| [**Cunknown**](cunknown-cunknown.md)                                       | Konstruktormethode.                                                |
| [**~ Cunknown**](cunknown--cunknown.md)                                    | Dekonstruktormethode. Virtu.                                        |
| [**GetOwner**](cunknown-getowner.md)                                       | Ruft einen Zeiger auf das steuernde **IUnknown**-Element ab.                    |
| Inondelegatingunknown-Methoden                                               | BESCHREIBUNG                                                        |
| [**Nondelegatingadressf**](cunknown-nondelegatingaddref.md)                 | Erhöht den Verweis Zähler.                                    |
| [**Nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) | Ruft einen Schnittstellen Zeiger ab und erhöht den Verweis Zähler. |
| [**Nondelegatingrelease**](cunknown-nondelegatingrelease.md)               | Verringert den Verweis Zähler.                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 




