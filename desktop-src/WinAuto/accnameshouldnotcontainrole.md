---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f09bd9ccdf27c5f52a45466b6b8145cfe23248cc175777f57202aac6530791
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899730"
---
# <a name="accnameshouldnotcontainrole"></a>AccNameShouldNotContainRole

## <a name="text"></a>Text

Der Name des Elements ( {0} ) darf nicht den Text der Rolle des Elements ( ) enthalten. {1}

## <a name="type"></a>type

Warnung

## <a name="description"></a>BESCHREIBUNG

Der Name eines Elements enthält die MSAA-Rolle oder den UIA-Steuerungstyp. Diese Warnung kann beispielsweise auftreten, wenn die [**get \_ accName-Methode,**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) die zum Abrufen des MSAA-Namens eines Elements verwendet wird, "ROLE \_ SYSTEM \_ SCROLLBAR" \_ zurückgibt. \*

Dieses Problem verursacht Probleme für Personen, die sich auf eine Sprachausgabe und Tastatur für die Navigation verlassen, da die Rolle zweimal gelesen wird, oder sie kann für Benutzer nicht angekündigt oder nicht intuitiv sein.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Das Element oder sein übergeordnetes Element weist einen falsch zugewiesenen Namen oder eine falsch zugewiesene Bezeichnung auf.
-   Das Element oder sein übergeordnetes Element hat einen Standardnamen, der nicht in einen Anzeigenamen geändert wurde. Zum Beispiel: Button1.
-   Ein Entwickler weiß nicht, dass Sprachausgaben Namen lesen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name-Eigenschaft](name-property.md)
</dt> </dl>

 

 




