---
title: ControlShouldHaveValue
description: ControlShouldHaveValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ced460fac38552e0b82396e6bbbcf92e90c341e40b289e332a3f188c7e4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998740"
---
# <a name="controlshouldhavevalue"></a>ControlShouldHaveValue

## <a name="text"></a>Text

Ein Steuerelement mit der Rolle {0} "" sollte einen Wert haben, \_ "get accValue" ist jedoch nicht implementiert.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Ein Element stellt einen Wert nicht wie erwartet basierend auf der zugewiesenen MSAA-Rolle dar, was bedeutet, dass die [**get \_ accValue-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) für das Element nicht implementiert ist. Beispielsweise sollten alle folgenden MSAA-Rollen einen Wert liefern.

-   KOMBINATIONSFELD \_ \_ "ROLLENSYSTEM"
-   \_ \_ ROLLENSYSTEM-IPADDRESS
-   ROLE \_ SYSTEM \_ LINK
-   ROLE \_ SYSTEM \_ OUTLINEITEM
-   STATUSLEISTE \_ DES \_ ROLLENSYSTEMS
-   \_ \_ ROLLENSYSTEMSCHIEBEREGLER
-   ROLE \_ SYSTEM \_ SPINBUTTON
-   \_ \_ ROLLENSYSTEM-BILDLAUFLEISTE
-   \_ \_ ROLLENSYSTEMTEXT

Dieses Problem ist ein Problem für Benutzer, die für die Navigation eine Sprachausgabe und Tastatur verwenden, da ein Element mit einem systeminternen Wert in der Lage sein muss, diesen Wert einem Benutzer zu melden.

## <a name="possible-causes"></a>Mögliche Ursachen

Für das Element oder das übergeordnete Element ist eine MSAA-Rolle nicht angemessen festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible::get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Objektrollen**](object-roles.md)
</dt> </dl>

 

 




