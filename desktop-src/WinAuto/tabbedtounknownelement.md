---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5acee341066ee5a456d412554ead3342c8513ae89e50a056a2372a291b0a88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052398"
---
# <a name="tabbedtounknownelement"></a>TabbedToUnknownElement

## <a name="text"></a>Text

Die Tabulatoren wurden zu einem Element außerhalb des Ziel-hwnds gelaufen.

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Die Verwendung der Standardtastaturnavigation (TAB oder UMSCHALT+TAB) bewirkt, dass der Fokus außerhalb des HWND des Überprüfungsziels verschoben wird.

AccChecker verschiebt die Elementstruktur zum HWND der obersten Ebene für das ausgewählte Überprüfungsziel, bevor Überprüfungsaufgaben ausgeführt werden. Dadurch wird die Anzahl der fehlerverwendigen Fehler reduziert, die generiert werden, wenn ein für die Überprüfung ausgewähltes HWND Teil eines komplexeren Clientbereichs ist.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Für das Überprüfungsziel ist keine Tabulatorimplementierung erforderlich, um vollständige Funktionen bereitstellen zu können.
-   Die Benutzerinteraktion während der Überprüfung, z. B. das Verschieben des Fokus auf ein HWND ohne Ziel, beeinträchtigt den Überprüfungsprozess.

 

 




