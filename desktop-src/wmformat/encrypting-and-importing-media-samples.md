---
title: Verschlüsseln und Importieren von Medien Beispielen
description: Verschlüsseln und Importieren von Medien Beispielen
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- Windows Media-Format-SDK, DRM-Import
- SDK für Windows Media-Format, importieren
- Windows Media-Format-SDK, Verschlüsseln von Medien Beispielen
- Digital Rights Management (DRM), importieren
- DRM (Digital Rights Management), importieren
- Digital Rights Management (DRM), Verschlüsseln von Medien Beispielen
- DRM (Digital Rights Management), Verschlüsseln von Medien Beispielen
- Erweiterte APIs für den DRM-Client, Import
- Erweiterte Client-APIs, importieren
- Erweiterte APIs für den DRM-Client, Verschlüsseln von Medien Beispielen
- Erweiterte Client-APIs, Verschlüsseln von Medien Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473db9580990b62818842aaa5eeea3e82f38c5ad
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389863"
---
# <a name="encrypting-and-importing-media-samples"></a>Verschlüsseln und Importieren von Medien Beispielen

Sie müssen für jedes Medien Beispiel, das Sie mithilfe von Windows Media DRM verschlüsseln, einen Salt-Wert generieren, der streng größer als der vorherige ist (monoton erhöht). Verwenden Sie den neuen Salt-Wert, um einen transitiven Verschlüsselungsschlüssel zu erstellen, indem Sie den SHA-1-Verschlüsselungsalgorithmus auf den Initialisierungs Vektor anwenden, der mit dem Salt-Wert verkettet ist.

Verschlüsseln Sie anschließend das Beispiel gemäß dem RC4-Algorithmus, indem Sie den generierten vorübergehendes-Schlüssel verwenden. Bevor das Beispiel an das SDK übermittelt wird, muss die Anwendung den Salt-Wert dem Beispiel zuordnen, indem ein Erweiterungs Attribut festgelegt wird.

Hier finden Sie die Schritte zum Verschlüsseln von Medien Beispielen:

1.  Ruft die **QueryInterface** -Methode des Sample-Objekts auf, um die [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) -Schnittstelle abzurufen.
2.  Erhöhen Sie den Salt-Wert.
3.  Verschlüsseln Sie das Beispiel mit einem RC1-Verschlüsselungsalgorithmus. Für die Verschlüsselung erstellen Sie einen Schlüssel, indem Sie den Initialisierungs Vektor und den Salt-Wert verketten.
4.  Geben Sie den Salt-Wert für das SDK durch Aufrufen von [**inssbuffer:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty)an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Import**](drm-import.md)
</dt> <dt>

[**Beispiel für eine Beispiel Verschlüsselung für Medien**](media-sample-encryption-example.md)
</dt> </dl>

 

 




