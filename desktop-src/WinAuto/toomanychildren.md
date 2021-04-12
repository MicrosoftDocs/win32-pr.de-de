---
title: "\"Zu untergeordnete Elemente\""
description: "\"Zu untergeordnete Elemente\""
ms.assetid: BF667CDC-C1F9-44B2-B64C-CD7F085CA364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e0eee0c29d0d5ee4cdfe66ee5b61aef4b31b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206833"
---
# <a name="toomanychildren"></a>"Zu untergeordnete Elemente"

## <a name="text"></a>Text

Suche nach weiteren neben geordneten Elementen nach dem Suchen nach neben geordneten Elementen beendet {0} Mögliche falsche Struktur

## <a name="type"></a>type

Warnung

## <a name="description"></a>BESCHREIBUNG

Die Elementstruktur kann zyklisch sein, und die Baum Tiefe ist unendlich.

Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da Sie einen Zirkel Verweis oder eine Endlosschleife eingeben.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Der Entwurf der Anwendung oder des Steuer Elements ist möglicherweise zu komplex. Diese Warnung wird möglicherweise für Listenansicht-Steuerelemente angezeigt, die über eine große Anzahl von Elementen verfügen. In diesen Fällen können Sie diese Warnung in der Regel ignorieren.
-   Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




