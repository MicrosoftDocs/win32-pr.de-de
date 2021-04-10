---
description: Das Address-Objekt stellt eine Entität dar, die Aufrufe ausführen oder empfangen kann.
ms.assetid: ab6db262-f99e-4027-9525-7597fcf02e72
title: Address-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ae91e70d6d8efb56321ca4619c6eb973799024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866615"
---
# <a name="address-object"></a>Address-Objekt

Das Address-Objekt stellt eine Entität dar, die Aufrufe ausführen oder empfangen kann. Dieses Objekt macht Schnittstellen und Methoden verfügbar, mit denen eine Anwendung eine Reihe von Vorgängen ausführen kann, wie z. b.:

-   Ermitteln, ob eine angegebene Adresse einen bestimmten Satz von Medientyp Anforderungen unterstützen kann.
-   Listet die derzeit der Adresse zugeordneten Aufrufe auf.
-   Aufrufe erstellen oder weiterleiten.
-   Den Namen des zugeordneten Dienstanbieters erhalten.
-   Wenn ein Medien Dienstanbieter vorhanden ist, erhalten Sie Schnittstellen Zeiger, die eine ausführliche Terminal Bearbeitung ermöglichen.
-   Dient zum erhalten und Festlegen anderer Informationen, z. b. ob eine Nachricht wartet.

Die meisten Adressen sind einem Terminal zugeordnet, dies ist jedoch nicht gleichmäßig der Fall. Ein Remote-TSP, der den Zugriff auf die Geräte auf einem Server ermöglicht, verfügt beispielsweise über eine Adresse auf dem lokalen Computer, aber nicht über ein Terminal. Einem Modem losen Modem ist auch kein Terminal mit seiner Adresse zugeordnet.

Wenn einer Adresse kein Terminal zugeordnet ist, wird die [**itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) -Schnittstelle für das Objekt nicht verfügbar gemacht.

Das Beispiel zum [Auswählen eines Adress](select-an-address.md) Codes zeigt den grundlegenden Prozess zum Abrufen eines Adress Objekt Zeigers.

Eine Liste aller dem Adress Objekt zugeordneten Schnittstellen finden Sie unter [Adress Objekt Schnittstellen](address-object-interfaces.md) .

 

 
