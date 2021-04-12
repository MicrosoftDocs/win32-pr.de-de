---
title: Auflisten von Lizenzen im lokalen Lizenz Speicher
description: Auflisten von Lizenzen im lokalen Lizenz Speicher
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows Media-Format-SDK, Auflisten von Lizenzen
- Windows Media-Format-SDK, Lizenzen
- Windows Media-Format-SDK, lokaler Lizenz Speicher
- Digital Rights Management (DRM), Auflisten von Lizenzen
- DRM (Digital Rights Management), Auflisten von Lizenzen
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), lokaler Lizenz Speicher
- DRM (Digital Rights Management), lokaler Lizenz Speicher
- Erweiterte APIs für den DRM-Client, Auflisten von Lizenzen
- Erweiterte Client-APIs, Auflisten von Lizenzen
- Erweiterte APIs für den DRM-Client, Lizenzen
- Erweiterte Client-APIs, Lizenzen
- Erweiterte APIs für den DRM-Client, lokaler Lizenz Speicher
- Erweiterte Client-APIs, lokaler Lizenz Speicher
- Lizenzen, auflisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b1384e08a6789fedca9704f36ad8da1e31b4ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388127"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a>Auflisten von Lizenzen im lokalen Lizenz Speicher

Die Enumeration ist ein Prozess zum erhalten von Informationen zu den Lizenzen im lokalen Lizenz Speicher, indem Sie nacheinander nacheinander durchlaufen werden. Sie können eine Lizenzierungs Enumeration erstellen, indem Sie die [**iwmdrmlicenaberation**](iwmdrmlicensemanagement-createlicenseenumeration.md)aufrufen.

Der häufigste Grund für das Auflisten von Lizenzen im Speicher ist das Auffinden einer bestimmten Lizenz für das Entschlüsseln einiger Inhalte.

Die [**iwmdrmlicense**](iwmdrmlicense.md) -Schnittstelle dient sowohl als Portal für die einzelnen Lizenz Ergebnisse als auch als Enumerator. Wenn die Lizenz-Enumeration erstellt wird, wird die erste Lizenz in der Liste in die **iwmdrmlicense** -Schnittstelle geladen. Die meisten Methoden von **iwmdrmlicense** ermöglichen es Ihnen, Informationen über die Lizenz zu erhalten oder Objekte zu erstellen, um Inhalte basierend auf der Lizenz zu verschlüsseln oder zu entschlüsseln. Es gibt jedoch zwei Methoden, die die Enumeration steuern: [**GetNext**](iwmdrmlicense-getnext.md) und [**resstenumeration**](iwmdrmlicense-resetenumeration.md). **GetNext** lädt die nächste Lizenz in der Liste in die-Schnittstelle. **Resegtenumeration** gibt die Enumeration in den Zustand zurück, in dem Sie sich bei der ersten Erstellung befand. Wenn die Enumeration zurückgesetzt wird, wird die erste Lizenz in der Liste wieder in die **iwmdrmlicense** -Schnittstelle geladen.

Wenn Sie die letzte Lizenz in der Liste erreicht haben, gibt der nächste **GetNext** -Befehl \_ einen Fehler ohne \_ Weitere Elemente zurück \_ .

Wenn Ihre Anwendung eine Aktion mit dem von DRM behandelten Inhalt ausführt, sollten Sie die Lizenzen im lokalen Lizenz Speicher auf die Rechte und auf andere einschränkende Faktoren (z. b. Ausgabe Schutz Ebenen) überprüfen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen aus Lizenzen im lokalen Lizenz Speicher erhalten**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




