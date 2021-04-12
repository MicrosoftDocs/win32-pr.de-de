---
title: Incorrectroundtrip
description: Incorrectroundtrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f154c0ccc0fff9bb654b94ef9d0807aa459d4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207130"
---
# <a name="incorrectroundtrip"></a>Incorrectroundtrip

## <a name="text"></a>Text

Rufen Sie auf, um zu über navigieren ((Klicken Sie auf "Wiederholen", um den Vorgang erneut auszuführen:), 1, navDir \_ Next), dann "accNavigate ((Open), 2, navDir \_ Previous"), sollte zurückgegeben werden, um wieder an Sie zu erinnern: (childID = 1)

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

durch die Verwendung von [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) zum Durchlaufen der Elementstruktur des Überprüfungs Ziels wird das gleiche Start Element nicht zurückgegeben, wenn die Richtung der Traversierung umgekehrt wird.

![Beispiel für eine ungültige MSAA-Implementierung, die eine falsche Roundtrip-Navigation verursacht hat](images/accchecker-invalid-round-trip.png)

Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da das Durchlaufen von Elementen möglicherweise erratisch und unvorhersagbar ist.

## <a name="possible-causes"></a>Mögliche Ursachen

Eine falsche oder ungültige MSAA-Implementierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




