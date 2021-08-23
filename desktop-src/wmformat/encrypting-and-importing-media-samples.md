---
title: Beispiele zum Verschlüsseln und Importieren von Medien
description: Beispiele zum Verschlüsseln und Importieren von Medien
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- Windows Medienformat-SDK, DRM-Import
- Windows Media Format SDK,import
- Windows Medienformat-SDK, Verschlüsseln von Medienbeispielen
- Digital Rights Management (DRM), Importieren
- DRM (Digital Rights Management), Import
- Digital Rights Management (DRM), Verschlüsseln von Medienbeispielen
- DRM (Digital Rights Management), Verschlüsseln von Medienbeispielen
- ERWEITERTE APIs des DRM-Clients,Import
- Erweiterte Client-APIs,Import
- Erweiterte DRM-Client-APIs, Verschlüsseln von Medienbeispielen
- Erweiterte Client-APIs, Verschlüsseln von Medienbeispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed604fc114feed6bd308b9a89c6bde6d6c96abeb9e88a7b9ace19d553de1596
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658840"
---
# <a name="encrypting-and-importing-media-samples"></a>Beispiele zum Verschlüsseln und Importieren von Medien

Für jedes Medienbeispiel, das Sie mithilfe von Windows Media DRM verschlüsseln, müssen Sie einen Salt-Wert generieren, der strikt größer als der vorherige wert ist (monoton erhöhend). Verwenden Sie den neuen Salt-Wert, um einen vorübergehenden Verschlüsselungsschlüssel zu erstellen, indem Sie den SHA-1-Verschlüsselungsalgorithmus auf den Initialisierungsvektor anwenden, der mit dem Salt-Wert verkettet ist.

Verschlüsseln Sie als Nächstes das Beispiel gemäß dem RC4-Algorithmus mithilfe des generierten vorübergehenden Schlüssels. Bevor das Beispiel an das SDK übergeben wird, muss Ihre Anwendung den Salt-Wert dem Beispiel zuordnen, indem ein Erweiterungsattribut angegeben wird.

Hier sind die Schritte zum Verschlüsseln von Medienbeispielen:

1.  Rufen Sie **die QueryInterface-Methode** des Beispielobjekts auf, um die [**INSSBuffer3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) zu erhalten.
2.  Erhöhen Sie den Saltwert.
3.  Verschlüsseln Sie das Beispiel mit einem RC1-Verschlüsselungsalgorithmus. Für die Verschlüsselung erstellen Sie einen Schlüssel, indem Sie den Initialisierungsvektor und den Salt-Wert verketten.
4.  Geben Sie den Salt-Wert für das SDK an, indem [**Sie INSSBuffer::SetProperty aufrufen.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Import**](drm-import.md)
</dt> <dt>

[**Beispiel für Medienbeispielverschlüsselung**](media-sample-encryption-example.md)
</dt> </dl>

 

 




