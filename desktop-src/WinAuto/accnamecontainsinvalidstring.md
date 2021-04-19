---
title: Accnamecontainsinvalidstring
description: Accnamecontainsinvalidstring
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670672769c22cba556c164b8d03b2e9148fb8b1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338618"
---
# <a name="accnamecontainsinvalidstring"></a>Accnamecontainsinvalidstring

## <a name="text"></a>Text

"accName" darf die Zeichenfolge nicht enthalten. {0}

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Der Name eines Elements enthält ungültige Zeichen (diese Zeichen werden durch die Zugriffs Prüfung ersetzt). Beispielsweise gibt die [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) -Methode, die zum Abrufen des MSAA-Namens eines Elements verwendet wird, eine Zeichenfolge zurück, die Tabulator-, Zeilen-oder Zeichen-und Zeichen enthält.

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da ein Element möglicherweise einen nicht Aussage fähigen, nicht intuitiven Namen hat.

## <a name="possible-causes"></a>Mögliche Ursachen

Dem Element oder seinem übergeordneten Element ist ein falsch zugewiesener Name oder eine Bezeichnung zugewiesen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name-Eigenschaft](name-property.md)
</dt> </dl>

 

 




