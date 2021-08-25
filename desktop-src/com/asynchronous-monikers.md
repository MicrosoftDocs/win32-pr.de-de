---
title: Asynchrone Moniker
description: Asynchrone Moniker
ms.assetid: 24c50f7b-f085-4086-aa44-81e5cab011cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9e9b5e427df882b7e0be84507b79c9113a46e44dad614e571a831fedecedff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859650"
---
# <a name="asynchronous-monikers"></a>Asynchrone Moniker

Die OLE-Monikerarchitektur bietet ein konsistentes, erweiterbares Programmiermodell für die Arbeit mit Internetobjekten, stellt Methoden zum Analysieren von Namen bereit, stellt URLs (Universal Resource Locators) als druckbare Namen dar und sucht und bindet die durch URL-Zeichenfolgen dargestellten Objekte. (Siehe auch [URL-Moniker.)](url-monikers.md) Ole-Standardmoniker (insbesondere Element-, Datei- und Zeigermoniker) sind jedoch für das Internet ungeeignet, da sie synchron sind und nur dann einen Zeiger auf ein Objekt oder dessen Speicher zurückgeben, wenn alle Daten verfügbar sind. Abhängig von der Menge der herunterzuladenden Daten kann die synchrone Bindung die Benutzeroberfläche des Clients über einen längeren Zeitraum binden.

Das Internet erfordert neue Ansätze für den Anwendungsentwurf. Anwendungen sollten alle teuren Netzwerkvorgänge asynchron ausführen können, um zu vermeiden, dass die Benutzeroberfläche angehalten wird. Eine Anwendung sollte in der Lage sein, einen Vorgang auszulösen und bei vollständiger oder teilweiser Vervollständigung eine Benachrichtigung zu erhalten. An diesem Punkt sollte die Anwendung die Wahl haben, entweder mit dem nächsten Schritt des Vorgangs fortzufahren oder bei Bedarf zusätzliche Informationen bereitzustellen. Während ein Download fortgesetzt wird, sollte eine Anwendung auch in der Lage sein, Benutzern Statusinformationen und die Möglichkeit zur Verfügung zu stellen, den Vorgang jederzeit abzubrechen.

Asynchrone Moniker bieten diese Funktionen sowie verschiedene Ebenen des asynchronen Bindungsverhaltens, während sie Abwärtskompatibilität für Anwendungen bereitstellen, die kein asynchrones Verhalten haben oder nicht benötigen. Eine andere OLE-Technologie, der asynchrone Speicher, arbeitet mit asynchronen Monikern zusammen, um das asynchrone Herunterladen des persistenten Zustands eines Internetobjekts bereitzustellen. Der asynchrone Moniker löst den Bindungsvorgang aus und richtet die erforderlichen Komponenten ein, einschließlich Speicher- und Streamobjekte, Bytearrayobjekte und Benachrichtigungssenken. Sobald die Komponenten verbunden sind, wird der Moniker nicht mehr ausgeführt, und der Rest der Bindung wird hauptsächlich zwischen den Komponenten ausgeführt, die die asynchronen Speicherkomponenten implementieren, und dem -Objekt.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Asynchrone und synchrone Moniker](./asynchronous-vs.-synchronous-monikers.md)
-   [Asynchrone und synchrone Bindung](./asynchronous-vs.-synchronous-binding.md)
-   [Asynchrone und synchrone Storage](./asynchronous-vs.-synchronous-storage.md)
-   [Daten-Pull-Modell und Data-Push-Modell](./data-pull-model-vs.-data-push-model.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[URL-Moniker](url-monikers.md)
</dt> </dl>

 

 