---
description: Wenn Sie einen oder mehrere Dateitypen einer neuen Anwendung zuordnen möchten, müssen Sie für jeden Dateityp, den Sie der Anwendung zuordnen möchten, eine ProgID definieren.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Registrieren eines Dateityps für eine neue Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728cc48075ab1c2631f0a950059da65ae326ae79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979528"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a>Registrieren eines Dateityps für eine neue Anwendung

Wenn Sie einen oder mehrere Dateitypen einer neuen Anwendung zuordnen möchten, müssen Sie für jeden Dateityp, den Sie der Anwendung zuordnen möchten, eine ProgID definieren.

Führen Sie diese Schritte aus, um für jeden eindeutigen Dateityp, der von der Anwendung behandelt wird, eine ProgID zu erstellen.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Beachten Sie, dass einige Dateitypen über mehrere Erweiterungen verfügen, die auf dieselbe ProgID zeigen. Zum Beispiel:

-   **HKEY \_ Klassen \_ root** \\ **app. JPEG** (ProgID)
-   **HKEY \_ Klassen \_ root** \\ **. jpg** = app. JPEG (Dateityp Zuordnungen)
-   **HKEY \_ Klassen \_ root** \\ **. JPEG** = app. JPEG

### <a name="step-2"></a>Schritt 2:

Entfernen Sie die ProgID-Werte, wenn Sie das Programm installieren und deinstallieren.

### <a name="step-3"></a>Schritt 3:

Lassen Sie die Dateityp Zuordnungen zum Zeitpunkt der Deinstallation unverändert. Dies funktioniert, weil Dateityp Zuordnungen pro Benutzer in HKEY \_ -Klassen " \_ root. ext" gespeichert werden \\ , und das System identifiziert den Fall, in dem der ProgID-Wert fehlt, und ignoriert ihn. Wenn Dateityp Zuordnungen unverändert bleiben, ist es nicht erforderlich, dass bedingter Code vorhanden ist, der nur die Dateityp Zuordnung entfernt, wenn der Wert weiterhin auf Ihre ProgID verweist. Es ist wichtig, dies zu vermeiden, wenn es möglicherweise von einer anderen Anwendung geändert wurde, und Sie können den Wert daher nicht einfach entfernen.

### <a name="step-4"></a>Schritt 4:

Geben Sie einen eindeutigen Wert für die Dateityp Beschreibung jeder Dateityp-ProgID an, indem Sie eine der folgenden Aktionen ausführen:

-   Belassen Sie den Standardwert der ProgID leer. in diesem Fall verwendet das System die ext-Datei.
-   Geben Sie einen lokalisierten Wert über friendlytyadapame an, und stellen Sie aus Kompatibilitätsgründen mit alten Anwendungen, die die Registrierung direkt lesen, sicher, dass Sie den Standardwert der ProgID als Dateityp Beschreibung angeben (d. h. den gleichen Wert verwenden, auf den der friendlytykame in der englischen Ressource verweist).

## <a name="remarks"></a>Bemerkungen

Wenn Sie beabsichtigen, die Datei einer vorhandenen Anwendung zuzuordnen, suchen Sie in der Registrierung nach einer Anwendungs ProgID. Weitere Informationen finden Sie unter [Dateitypen](fa-file-types.md).

 

 



