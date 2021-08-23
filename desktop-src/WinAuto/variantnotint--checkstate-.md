---
title: VariantNotInt (CheckState)
description: VariantNotInt (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3334a3609e9d64c1bb7109cc6f5bb52a2d09f9f9ac18cc41abf5d761f8e939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052168"
---
# <a name="variantnotint-checkstate"></a>VariantNotInt (CheckState)

## <a name="text"></a>Text

Die von zurückgegebene {0} Variante sollte ein {1} sein, ist aber ein {2} .

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Ein Element gibt einen ungültigen MSAA-Zustand an. Beispielsweise sollte die [**get \_ accState-Methode,**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) die zum Abrufen des MSAA-Zustands eines Elements verwendet wird, einen ganzzahligen Wert zurückgeben, der eine der MSAA-Zustandskonst constants darstellt, aber stattdessen eine andere Variante zurückgibt.

Dieses Problem verursacht Probleme für Personen, die für die Navigation eine Sprachausgabe und Tastatur verwenden, da dem Benutzer möglicherweise ein falscher Elementzustand gemeldet wird.

## <a name="possible-causes"></a>Mögliche Ursachen

Für das Element oder das übergeordnete Element ist der MSAA-Zustand nicht angemessen festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible::get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Objektzustandskonst constants**](object-state-constants.md)
</dt> </dl>

 

 




