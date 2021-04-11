---
description: Übersicht über die Fehler Protokollierung
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Übersicht über die Fehler Protokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af82c35cdb34a238e280641015407c7a5d6f837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124369"
---
# <a name="overview-of-error-logging"></a>Übersicht über die Fehler Protokollierung

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Um Anwendungen maximale Flexibilität bei der Behandlung von Fehlern zu ermöglichen, verwenden [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md) einen Rückrufmechanismus. Die Anwendung implementiert eine Methode zum Protokollieren eines Fehlers. Wenn zur Laufzeit ein Fehler auftritt, ruft der die von Ihnen bereitgestellte Methode auf. Die-Methode übernimmt Parameter, die den Fehler beschreiben. Die Methode, mit der diese Informationen verwendet werden, ist Ihnen überstehen. (Es sollte jedoch so schnell wie möglich zurückgeben, oder es kann die Ausführung des Programms beeinträchtigen.)

Die Rückruf Methode für die Fehler Protokollierung ist in einer COM-Schnittstelle ( [**iamerrorlog**](iamerrorlog.md)) enthalten. Die Anwendung muss diese Schnittstelle implementieren. Wie alle COM-Schnittstellen erbt **iamerrorlog** die **IUnknown** -Schnittstelle, sodass die Anwendung dies ebenfalls implementieren muss.

Sie haben mehrere Möglichkeiten, diese COM-Schnittstellen zu implementieren. Sie können den Active Template Library (ATL) verwenden, der die vordefinierten Implementierungen der **IUnknown** -Methoden bereitstellt. DirectShow bietet auch eine C++-Basisklasse ( [**cunknown**](cunknown.md)), mit der eine COM-Schnittstelle leicht implementiert werden kann. Informationen zur Verwendung von **cunknown** finden Sie unter Gewusst [wie: Implementieren von IUnknown](how-to-implement-iunknown.md).

Der Beispielcode in diesem Artikel definiert eine eigenständige C++-Klasse, die sowohl **IUnknown** als auch **iamerrorlog** implementiert. Das Ergebnis ist kein echtes com-Objekt, da es **cokreateinstance** nicht unterstützt. Dieser Ansatz ist jedoch für den Zweck des Beispiels geeignet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Protokollierungs Fehler](logging-errors.md)
</dt> </dl>

 

 



