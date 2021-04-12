---
title: Variantnotint (CheckState)
description: Variantnotint (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206770"
---
# <a name="variantnotint-checkstate"></a>Variantnotint (CheckState)

## <a name="text"></a>Text

Die von zurückgegebene Variante {0} sollte ein sein, {1} aber ist {2} .

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Ein Element meldet einen ungültigen MSAA-Zustand. Beispielsweise sollte die [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) -Methode, die zum Abrufen des MSAA-Zustands eines Elements verwendet wird, einen ganzzahligen Wert zurückgeben, der eine der MSAA-Zustands Konstanten darstellt, sondern stattdessen eine andere Variante zurückgibt.

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da dem Benutzer ein falscher Element Zustand gemeldet werden könnte.

## <a name="possible-causes"></a>Mögliche Ursachen

Für das-Element oder das übergeordnete Element ist ein MSAA-Zustand unpassend festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: get- \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Objekt Zustands Konstanten**](object-state-constants.md)
</dt> </dl>

 

 




