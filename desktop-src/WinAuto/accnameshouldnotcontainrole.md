---
title: Accnameshouldnotcontainrole
description: Accnameshouldnotcontainrole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb91eeeb34d484c1f51cd0b7cd2d2947e86abda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714195"
---
# <a name="accnameshouldnotcontainrole"></a>Accnameshouldnotcontainrole

## <a name="text"></a>Text

Der Name des Elements ( {0} ) darf nicht den Text der Rolle des Elements () enthalten. {1}

## <a name="type"></a>type

Warnung

## <a name="description"></a>BESCHREIBUNG

Der Name eines Elements enthält die MSAA-Rolle oder den UIA-Steuer Elementtyp. Diese Warnung kann z. b. auftreten, wenn die [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) -Methode –, die verwendet wird, um den MSAA-Namen eines Elements abzurufen – "role \_ System \_ ScrollBar" zurückgibt \_ \* .

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme haben, da die Rolle zweimal gelesen wird, oder Sie ist möglicherweise für Benutzer nicht erklärbar oder nicht intuitiv.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Dem Element oder seinem übergeordneten Element ist ein falsch zugewiesener Name oder eine Bezeichnung zugewiesen.
-   Das Element oder das übergeordnete Element verfügt über einen Standardnamen, der nicht auf einen anzeigen Amen überarbeitet wurde. Zum Beispiel: Button1.
-   Ein Entwickler weiß nicht, dass die Bildschirm Sprachausgaben Lese Namen haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name-Eigenschaft](name-property.md)
</dt> </dl>

 

 




