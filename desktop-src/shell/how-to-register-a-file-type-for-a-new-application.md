---
description: Wenn Sie einer neuen Anwendung einen oder mehrere Dateitypen zuordnen möchten, müssen Sie eine ProgID für jeden Dateityp definieren, den Sie der Anwendung zuordnen möchten.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Registrieren eines Dateityps für eine neue Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de165d378d27c6891b681f95da7242b026844bd7734709ebd272c06edf40e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859660"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a>Registrieren eines Dateityps für eine neue Anwendung

Wenn Sie einer neuen Anwendung einen oder mehrere Dateitypen zuordnen möchten, müssen Sie eine ProgID für jeden Dateityp definieren, den Sie der Anwendung zuordnen möchten.

Um eine ProgID für jeden eindeutigen Dateityp zu erstellen, den Ihre Anwendung verarbeitet, verwenden Sie diese Schritte.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Beachten Sie, dass einige Dateitypen über mehrere Erweiterungen verfügen, die auf dieselbe ProgID verweisen. Zum Beispiel:

-   **HKEY \_ CLASSES \_ ROOT** \\ **App.jpeg** (Ihre ProgID)
-   **HKEY \_ CLASSES \_ ROOT** \\ **.jpg** = App.jpeg (die Dateitypzuordnungen)
-   **HKEY \_ CLASSES \_ ROOT** \\ **.jpeg** = App.jpeg

### <a name="step-2"></a>Schritt 2:

Entfernen Sie die ProgID-Werte, wenn Sie das Programm installieren und deinstallieren.

### <a name="step-3"></a>Schritt 3:

Lassen Sie die Dateitypzuordnungen zum Zeitpunkt der Deinstallation unverändert. Dies funktioniert, da Dateitypzuordnungen pro Benutzer in HKEY CLASSES ROOT .ext gespeichert werden \_ und das System den Fall \_ \\ identifiziert, in dem der ProgID-Wert fehlt, und ignoriert ihn. Wenn Sie Dateitypzuordnungen unverändert lassen, müssen Sie keinen bedingten Code verwenden, der nur dann die Dateitypzuordnung entfernt, wenn der Wert weiterhin auf Ihre ProgID verweist. Es ist wichtig, dies in Fällen zu vermeiden, in denen sie möglicherweise von einer anderen Anwendung geändert wurde und Sie den Wert daher nicht einfach entfernen können.

### <a name="step-4"></a>Schritt 4:

Geben Sie einen eindeutigen Wert für die Dateitypbeschreibung jedes Dateityps ProgID an, indem Sie einen der folgenden Schritte ausführen:

-   Lassen Sie den Standardwert der ProgID leer. In diesem Fall verwendet das System die EXT-Datei.
-   Geben Sie einen lokalisierten Wert über FriendlyTypeName an, und stellen Sie zur Kompatibilität mit alten Anwendungen, die die Registrierung direkt lesen, sicher, dass Sie den Standardwert der ProgID als Dateitypbeschreibung angeben (d. h. denselben Wert verwenden, auf den in der englischen Ressource friendlyTypeName verwiesen wird).

## <a name="remarks"></a>Hinweise

Wenn Sie die Datei einer vorhandenen Anwendung zuordnen möchten, suchen Sie eine ProgID der Anwendung in der Registrierung. Weitere Informationen finden Sie unter [Dateitypen.](fa-file-types.md)

 

 



