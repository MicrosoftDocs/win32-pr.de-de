---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acecf91e90f93ccb1d220e9b2d91cbaa012b8d436b18a910daa73bf6ca3f1fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860000"
---
# <a name="invalidrole"></a>InvalidRole

## <a name="text"></a>Text

Der von get \_ accRole zurückgegebene int ist keine gültige Rollenkonst constant, d.&160;B. ROLE \_ SYSTEM.\_\*

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Ein Element gibt eine ungültige MSAA-Rolle an. Die get [**\_ accRole-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) gibt z. B. einen ganzzahligen Wert zurück, der nicht einer gültigen Objektrolle-Konstante (z. B. ROLE \_ SYSTEM \_ LISTITEM) zukommt.

Dieses Problem verursacht Probleme für Benutzer, die eine Sprachausgabe und Tastatur für die Navigation verwenden, da Elemente für den Benutzer möglicherweise falsch identifiziert werden.

## <a name="possible-causes"></a>Mögliche Ursachen

Für das Element oder das übergeordnete Element ist eine MSAA-Rolle nicht angemessen festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible::get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Objektrollen**](object-roles.md)
</dt> </dl>

 

 




