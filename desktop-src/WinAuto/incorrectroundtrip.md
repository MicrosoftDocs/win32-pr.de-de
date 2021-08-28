---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17f0ca96496a9e98c1068354e3a9efda27ca8cb0993f6f924ea68ef7d0c1436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644735"
---
# <a name="incorrectroundtrip"></a>IncorrectRoundTrip

## <a name="text"></a>Text

Call to accNavigate((Click Snooze to be reminded in:), 1, NAVDIR \_ NEXT), then accNavigate((Open), 2, NAVDIR PREVIOUS), should should returned Click Snooze to be reminded \_ again in:(ChildId=1), but returned Click Snooze to be reminded again in:

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Wenn [**accNavigate zum**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) Durchlaufen der Elementstruktur des Überprüfungsziels verwendet wird, wird nicht das gleiche Startelement zurückgeben, wenn die Richtung des Durchlaufs umgekehrt wird.

![Beispiel für eine ungültige msaa-Implementierung, die eine falsche Roundtripnavigation verursacht hat](images/accchecker-invalid-round-trip.png)

Dieses Problem kann zu Navigationsproblemen für automatisierte Tools führen, da das Durchlaufen von Elementen möglicherweise unvorhergesehen und unvorhersehbar ist.

## <a name="possible-causes"></a>Mögliche Ursachen

Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




