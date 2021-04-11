---
title: Controlschuldhavevalue
description: Controlschuldhavevalue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b078712319ffcfde386df519837ba467ca2fcf4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206922"
---
# <a name="controlshouldhavevalue"></a>Controlschuldhavevalue

## <a name="text"></a>Text

Ein Steuerelement mit der Rolle {0} muss über einen Wert verfügen, aber get \_ accValue ist nicht implementiert.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Ein Element stellt auf der Grundlage der zugewiesenen MSAA-Rolle nicht erwartungsgemäß einen Wert bereit. Dies impliziert, dass das Element nicht über die [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) -Methode verfügt. Die folgenden MSAA-Rollen sollten beispielsweise alle einen Wert bereitstellen.

-   Kombinations \_ Feld "Rollen System" \_
-   Rollen \_ System- \_ IPAddress
-   Rollen \_ System \_ Link
-   Rollen \_ System \_ outlineitem
-   Rollen \_ System- \_ ProgressBar
-   \_ \_ Schieberegler für Rollen System
-   \_SpinButton für Rollen System \_
-   Rollen \_ System- \_ Scrollleiste
-   Rollen \_ System \_ Text

Dieses Problem ist ein Problem für Personen, die sich auf einen Bildschirm und eine Tastatur für die Navigation verlassen, da ein Element mit einem systeminternen Wert in der Lage sein muss, diesen Wert an einen Benutzer zu melden.

## <a name="possible-causes"></a>Mögliche Ursachen

Für das-Element oder das übergeordnete Element ist eine MSAA-Rolle inadäquat festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Objekt Rollen**](object-roles.md)
</dt> </dl>

 

 




