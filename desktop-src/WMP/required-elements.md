---
title: Erforderliche Elemente
description: Erforderliche Elemente
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Windows Media Player Mobile Skins, Elemente
- Skins, Elemente
- Skindefinitionsdateien, Elemente
- Elements, Skindefinitionsdateien
- elements,Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18433e20c914cdc4b276857f97aab6a692d1d11c811660c73620b09a5b9a0f55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746309"
---
# <a name="required-elements"></a>Erforderliche Elemente

Sie müssen die folgenden Elemente in der Skindefinitionsdatei angeben:

-   **Header.** Der Hauptheader der Skindefinitionsdatei ist erforderlich. Informationen zur Headerversion finden Sie in der Tabelle im Abschnitt [Erstellen einer Skindefinitionsdatei.](creating-a-skin-definition-file.md)
-   **Beschreibungsabschnitt.** Der Abschnitt Beschreibung ist erforderlich, wenn Skins für Windows Media Player 9-Serie für Windows Mobile erstellt werden. Es muss der erste Abschnitt in der Skindefinitionsdatei sein und gültige Werte für Dimensionen angeben. Das Angeben eines Werts für Orientation ist optional.
-   **Bitmaps-Abschnitt.** Der Abschnitt Bitmaps ist erforderlich. Darüber hinaus müssen im Abschnitt Bitmaps gültige Namen für Hintergrund-, Deaktiviert-, Push-, Regions- und Superbilddateien angegeben werden.
-   **Bilddateien.** Sie müssen Hintergrund-, Deaktiviert-, Push-, Regions- und Superbilddateien als Teil Ihrer Skin angeben. Wenn Sie Skins für Windows Media Player 10 Mobile oder höher erstellen, müssen Sie keine Regions- oder Superimagedateien einschließen.

Wenn Sie eine Skin mit nur definierten Bildern erstellen, ist die Skin sichtbar, bietet dem Benutzer jedoch keine sinnvollen Funktionen. Wenn Sie sich dafür entscheiden, eine Skin ohne Schaltflächen zu erstellen, um möglicherweise zu verhindern, dass der Benutzer bestimmte Inhalte überspringt, sollten Sie beachten, dass es möglicherweise weiterhin möglich ist, die Funktionalität den Hardwareschaltflächen auf dem Gerät zuzuordnen.

Daumendateien sind erforderlich, und Ihre Trackleisten können nicht ohne Daumen verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skindefinitionsdatei**](skin-definition-file-mobile.md)
</dt> </dl>

 

 




