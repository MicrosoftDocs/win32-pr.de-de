---
title: Erforderliche Elemente
description: Erforderliche Elemente
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Windows Media Player Mobile Skins, Elemente
- Skins, Elemente
- Skin-Definitions Dateien, Elemente
- Elemente, Skin-Definitions Dateien
- Elemente, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1f05ba51b83fad6585d24c3ad19830598b8975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710877"
---
# <a name="required-elements"></a>Erforderliche Elemente

Sie müssen die folgenden Elemente in der Skin-Definitionsdatei angeben:

-   **Header.** Der Header der Haupt Skin-Definitionsdatei ist erforderlich. Informationen zur Header Version finden Sie in der Tabelle im Abschnitt [Erstellen einer Skin-Definitionsdatei](creating-a-skin-definition-file.md) .
-   **Abschnitt Beschreibung.** Der Abschnitt Beschreibung ist erforderlich, wenn Sie Skins für Windows Media Player 9-Reihe für Windows Mobile erstellen. Dies muss der erste Abschnitt in der Skin-Definitionsdatei sein, und es muss gültige Werte für Dimensionen angegeben werden. Die Angabe eines Werts für die Ausrichtung ist optional.
-   **Abschnitt Bitmaps.** Der Abschnitt "Bitmaps" ist erforderlich. Außerdem muss im Abschnitt Bitmaps gültige Namen für die Dateien background, deaktiviert, per pushübertragung, Region und Super Image angegeben werden.
-   **Bilddateien.** Sie müssen Hintergrund-, deaktivierte, pushdateien, Regions-und Super Bilddateien als Teil ihrer Skin bereitstellen. Wenn Sie Skins für Windows Media Player 10 Mobile oder höher erstellen, müssen Sie keine Regions-oder Super Image Dateien einschließen.

Wenn Sie eine Skin erstellen, für die nur Bilder definiert sind, wird die Skin angezeigt, bietet dem Benutzer jedoch keine sinnvollen Funktionen. Wenn Sie sich dafür entscheiden, eine Skin ohne Schaltflächen zu erstellen, um zu verhindern, dass der Benutzer bestimmte Inhalte überspringt, beachten Sie, dass es möglicherweise dennoch möglich ist, die Funktionalität den Hardware Schaltflächen auf dem Gerät zuzuordnen.

Thumb-Dateien sind erforderlich, und ihre trackbars können nicht ohne Daumen verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Definitionsdatei**](skin-definition-file-mobile.md)
</dt> </dl>

 

 




