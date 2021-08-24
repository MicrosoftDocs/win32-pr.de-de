---
title: Die Edge-Benutzeroberfläche wird in "In-Out-In"- und "Trägheit"-Szenarien unterdrückt.
description: Die Edge-Benutzeroberfläche wird in "In-Out-In"- und "Trägheit"-Szenarien unterdrückt.
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec032fa97f54fc1b1325055c9b02bdebe9e817b0f85971c2e2a7062e93c284c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593960"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a>Die Edge-Benutzeroberfläche wird in "In-Out-In"- und "Trägheit"-Szenarien unterdrückt.

## <a name="platform"></a>Plattform

<dl> Clients – Windows 8.1  
</dl>

## <a name="description"></a>Beschreibung

Es gibt einige Fälle, in denen Benutzer versehentlich die Edge-Benutzeroberfläche aufrufen können (Charms, App-Leiste, App-Wechsel). Wir haben ein Feature eingeführt, mit dem Entwickler ihre Benutzeroberfläche für den gesamten Bildschirm entwerfen können, ohne Sichten (z. B. Rahmen) zu leisten, um zu verhindern, dass der Benutzer versehentlich auf die Ränder trifft.

Es gibt zwei Fälle, die am häufigsten zu unbeabsichtigten Kantenwischen führen können:

-   Beim schnellen Schwenken kann die Geschwindigkeit und Ungenauigkeit der Interaktion gelegentlich dazu führen, dass sie vom Rand des Bildschirms ein-
-   Wenn Benutzer den Bildschirmbereich schnell verlassen und erneut aufrufen, während sie sich mit dem Finger z. B. in einer Zeichnungs-App einschließen, kann dieses ein- und ausgehende Verhalten versehentlich die Edge-Benutzeroberfläche auslösen und die Benutzeroberfläche unterbrechen.

Um die Benutzer- und Entwicklererfahrung zu verbessern, wird die Edge-Benutzeroberfläche jetzt in zwei bestimmten Instanzen unterdrückt:

-   Wenn ein Benutzer in einer Anwendung schwenkt, die DManip Inertia unterstützt und während der Trägheit außerhalb des Bildschirms wischt, wird die Edge-Benutzeroberfläche nicht innerhalb eines Timeoutfensters aufgerufen.
-   Auf zertifizierten Geräten wird die Edge-Benutzeroberfläche nicht aufgerufen, wenn ein Benutzer innerhalb des Bildschirms schnell von außerhalb des Bildschirms nach außen wischt und innerhalb bestimmter Parameter wieder zurück in den Bildschirm (In-Out-In-Bewegung) wischt.

## <a name="manifestations"></a>Manifestationen

Benutzer, die während der Verwendung einer App schnell über den Rand wischen, sehen eine Verringerung des unbeabsichtigten Edgeaufrufs.

## <a name="solution"></a>Lösung

Entwickler sollten diese Entschärfungen im Hinterkopf behalten und in der Lage sein, den Vollbildmodus zu verwenden, ohne zu befürchten, dass Benutzer versehentlich die Edge-Benutzeroberfläche auslösen, während sie mit der Anwendung entlang des Edgebereichs interagieren.

 

 




