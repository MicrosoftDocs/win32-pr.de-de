---
title: Asynchrone Moniker
description: Asynchrone Moniker
ms.assetid: 24c50f7b-f085-4086-aa44-81e5cab011cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19323af3a972a2b83a290176a4b26fb79382da0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106340943"
---
# <a name="asynchronous-monikers"></a>Asynchrone Moniker

Die OLE-monikerarchitektur bietet ein konsistentes, erweiterbares Programmiermodell für das Arbeiten mit Internet Objekten, das Bereitstellen von Methoden zum Durchsuchen von Namen, das darstellen von URLs (Universal Resource Locators) als Druck Bare Namen sowie das Suchen und Binden von Objekten, die durch URL-Zeichen folgen dargestellt werden. (Siehe auch [URL-Moniker](url-monikers.md).) Standard-OLE-Moniker (insbesondere Element-, Datei-und zeigermoniker) sind jedoch für das Internet ungeeignet, da sie synchron sind. Sie geben einen Zeiger auf ein Objekt oder den Speicher nur zu dem Zeitpunkt zurück, an dem alle Daten verfügbar sind. Abhängig von der Menge der Daten, die heruntergeladen werden sollen, kann die Bindung synchron die Benutzeroberfläche des Clients über längere Zeiträume hinweg binden.

Das Internet erfordert neue Ansätze für den Anwendungs Entwurf. Anwendungen sollten in der Lage sein, alle teuren Netzwerk Vorgänge asynchron auszuführen, um zu verhindern, dass die Benutzeroberfläche blockiert wird. Eine Anwendung sollte in der Lage sein, einen Vorgang zu initiieren und eine Benachrichtigung zu vollständigen oder partiellen Abschluss zu erhalten. An diesem Punkt sollte die Anwendung die Wahl haben, entweder mit dem nächsten Schritt des Vorgangs fortzufahren oder bei Bedarf zusätzliche Informationen bereitzustellen. Wenn ein Download fortgesetzt wird, sollte eine Anwendung auch in der Lage sein, den Benutzern Statusinformationen und die Möglichkeit zu geben, den Vorgang jederzeit abzubrechen.

Asynchrone Moniker stellen diese Funktionen sowie verschiedene Ebenen des asynchronen Bindungs Verhaltens bereit und bieten gleichzeitig eine Abwärtskompatibilität für Anwendungen, die entweder nicht über ein asynchrones Verhalten verfügen oder dieses nicht benötigen. Eine andere OLE-Technologie, asynchroner Speicher, funktioniert mit asynchronen Monikern, um das asynchrone herunterladen des permanenten Zustands eines Internet Objekts bereitzustellen. Der asynchrone Moniker löst den Bindungs Vorgang aus und richtet die erforderlichen Komponenten ein, einschließlich Speicher-und Streamobjekte, Bytearray-Objekte und Benachrichtigungs senken. Nachdem die Komponenten verbunden sind, wird der Moniker von der Art und Weise ausgeführt, und der Rest der Bindung wird hauptsächlich zwischen den Komponenten ausgeführt, die die asynchronen Speicherkomponenten und das-Objekt implementieren.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Asynchrone und synchrone Moniker](./asynchronous-vs.-synchronous-monikers.md)
-   [Asynchrone und synchrone Bindung](./asynchronous-vs.-synchronous-binding.md)
-   [Asynchroner und synchroner Speicher](./asynchronous-vs.-synchronous-storage.md)
-   [Datenpull-Modell und Data-Push Modell](./data-pull-model-vs.-data-push-model.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[URL-Moniker](url-monikers.md)
</dt> </dl>

 

 