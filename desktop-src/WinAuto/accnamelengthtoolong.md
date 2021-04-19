---
title: Accnamelengthtoolong
description: Accnamelengthtoolong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1efcb2b7d13c83a5972cb6e100d70500f9c5ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337184"
---
# <a name="accnamelengthtoolong"></a>Accnamelengthtoolong

## <a name="text"></a>Text

Der Element Name darf keine Zeichenfolge zurückgeben, die länger als Zeichen ist. {0}

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Der Name eines Elements enthält zu viele Zeichen. Beispielsweise gibt die [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) -Methode, die zum Abrufen des MSAA-Namens eines Elements verwendet wird, eine Zeichenfolge zurück, die größer ist als das Limit von 32000 Zeichen.

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da ein Element möglicherweise einen nicht Aussage fähigen, nicht intuitiven Namen hat.

## <a name="possible-causes"></a>Mögliche Ursachen

Dem Element oder seinem übergeordneten Element ist ein falsch zugewiesener Name oder eine Bezeichnung zugewiesen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name-Eigenschaft](name-property.md)
</dt> </dl>

 

 




