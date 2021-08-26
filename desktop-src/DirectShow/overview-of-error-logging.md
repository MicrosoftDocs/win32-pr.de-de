---
description: Übersicht über die Fehlerprotokollierung
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Übersicht über die Fehlerprotokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcde3e0366ffca12dfcb5674259273ba1bbf25c1feed9be3ead57fa64cc42dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904630"
---
# <a name="overview-of-error-logging"></a>Übersicht über die Fehlerprotokollierung

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Um Anwendungen maximale Flexibilität bei der Fehlerbehandlung zu bieten, verwendet [DirectShow Editing Services](directshow-editing-services.md) einen Rückrufmechanismus. Ihre Anwendung implementiert eine Methode zum Protokollieren eines Fehlers. Wenn zur Laufzeit ein Fehler auftritt, ruft DES die von Ihnen bereitgestellte Methode auf. Die -Methode verwendet Parameter, die den Fehler beschreiben. Was die -Methode mit diesen Informationen macht, liegt bei Ihnen. (Es sollte jedoch so schnell wie möglich zurückgeben, oder es kann die Ausführung des Programms beeinträchtigen.)

Die Rückrufmethode für die Fehlerprotokollierung ist in der COM-Schnittstelle [**IAMErrorLog enthalten.**](iamerrorlog.md) Ihre Anwendung muss diese Schnittstelle implementieren. Wie alle COM-Schnittstellen erbt **IAMErrorLog** die **IUnknown-Schnittstelle,** sodass Ihre Anwendung dies ebenfalls implementieren muss.

Sie haben mehrere Möglichkeiten, diese COM-Schnittstellen zu implementieren. Sie können die Active Template Library (ATL) verwenden, die Vorratimplementierungen der **IUnknown-Methoden** bietet. DirectShow stellt auch die C++-Basisklasse [**CUnknown**](cunknown.md)bereit, die die Implementierung einer COM-Schnittstelle vereinfacht. Informationen zur Verwendung von **CUnknown finden Sie** unter [Implementieren von IUnknown](how-to-implement-iunknown.md).

Der Beispielcode in diesem Artikel definiert eine eigenständige C++-Klasse, die sowohl **IUnknown** als auch **IAMErrorLog implementiert.** Das Ergebnis ist kein echtes COM-Objekt, da es **CoCreateInstance nicht unterstützt.** Dieser Ansatz ist jedoch für die Zwecke des Beispiels ausreichend.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Protokollierungsfehler](logging-errors.md)
</dt> </dl>

 

 



