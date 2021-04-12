---
title: Tabbedbackunknownelement
description: Tabbedbackunknownelement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612476d81779c882eeca807a9c3b82c41594f218
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388156"
---
# <a name="tabbedtounknownelement"></a>Tabbedbackunknownelement

## <a name="text"></a>Text

Tabstopps ist an ein Element außerhalb des Ziel-HWND gegangen.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Die Verwendung der Standardtastatur Navigation (Tab oder UMSCHALT + TAB) bewirkt, dass der Fokus außerhalb des HWND des Überprüfungs Ziels verschoben wird.

Die Zugriffs Prüfung verschiebt die Elementstruktur in das HWND der obersten Ebene für das ausgewählte Überprüfungs Ziel, bevor Überprüfungs Tasks ausgeführt werden. Dadurch wird die Anzahl falscher Fehler verringert, die generiert werden, wenn ein für die Überprüfung ausgewähltes HWND Teil eines komplexeren Client Bereichs ist.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Das Überprüfungs Ziel erfordert keine Tabstopps-Implementierung, um vollständige Funktionalität bereitzustellen.
-   Die Benutzerinteraktion während der Überprüfung, z. b. das Verschieben des Fokus auf ein nicht-Ziel-HWND, hat den Überprüfungs Vorgang beeinträchtigt.

 

 




