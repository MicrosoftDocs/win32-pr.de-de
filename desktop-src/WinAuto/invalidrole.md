---
title: Ungültig
description: Ungültig
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531aa9917bd68b615c2cd2457d7a24bfc4af336c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340818"
---
# <a name="invalidrole"></a>Ungültig

## <a name="text"></a>Text

Der von Get accRole zurückgegebene int-Wert \_ ist keine gültige Rollen Konstante, d. h. das Rollen \_ System.\_\*

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Ein Element meldet eine ungültige MSAA-Rolle. Beispielsweise gibt die [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) -Methode einen ganzzahligen Wert zurück, der keiner gültigen Objekt Rollen Konstante (z. b \_ . Role System \_ ListItem) zugeordnet wird.

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm und eine Tastatur für die Navigation verlassen, Probleme verursachen, da die Elemente für den Benutzer möglicherweise falsch identifiziert werden.

## <a name="possible-causes"></a>Mögliche Ursachen

Für das-Element oder das übergeordnete Element ist eine MSAA-Rolle inadäquat festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Objekt Rollen**](object-roles.md)
</dt> </dl>

 

 




