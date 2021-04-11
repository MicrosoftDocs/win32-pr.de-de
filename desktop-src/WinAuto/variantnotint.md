---
title: Variantnotint (checkrole)
description: Variantnotint (checkrole)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310151"
---
# <a name="variantnotint-checkrole"></a>Variantnotint (checkrole)

## <a name="text"></a>Text

Die von zurückgegebene Variante {0} sollte ein sein, {1} aber ist {2} .

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Ein Element meldet eine ungültige MSAA-Rolle. Beispielsweise sollte die [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) -Methode, die zum Abrufen der MSAA-Rolle eines Elements verwendet wird, einen ganzzahligen Wert zurückgeben, der eine der MSAA-Rollen Konstanten darstellt, sondern stattdessen eine andere Variante zurückgibt.

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm und eine Tastatur für die Navigation verlassen, Probleme verursachen, da die Elemente für den Benutzer möglicherweise falsch identifiziert werden.

## <a name="possible-causes"></a>Mögliche Ursachen

Für das-Element oder das übergeordnete Element ist eine MSAA-Rolle inadäquat festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Objekt Rollen**](object-roles.md)
</dt> </dl>

 

 




