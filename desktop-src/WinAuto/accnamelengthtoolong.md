---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9df4b9001460b9ad96cf5c987a0e8c744ec8df183901494311275052ea4146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327706"
---
# <a name="accnamelengthtoolong"></a>AccNameLengthTooLong

## <a name="text"></a>Text

Der Name des Elements darf keine Zeichenfolge zurückgeben, die länger als ein Zeichen {0} ist.

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Der Name eines Elements enthält zu viele Zeichen. Beispielsweise gibt die [**get \_ accName-Methode,**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) die zum Abrufen des MSAA-Namens eines Elements verwendet wird, eine Zeichenfolge zurück, die den Grenzwert von 32.000 Zeichen überschreitet.

Dieses Problem verursacht Probleme für Benutzer, die für die Navigation eine Sprachausgabe und Tastatur verwenden, da ein Element möglicherweise einen unvorhersetzbaren, nicht intuitiven Namen hat.

## <a name="possible-causes"></a>Mögliche Ursachen

Dem Element oder dem übergeordneten Element ist ein falsch zugewiesener Name oder eine falsch zugewiesene Bezeichnung zugewiesen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name-Eigenschaft](name-property.md)
</dt> </dl>

 

 




