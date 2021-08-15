---
title: Inkompatible ARIA-Bereichssteuerelementattribute
description: Inkompatible ARIA-Bereichssteuerelementattribute
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- AriaRangeControlAttributesIncompatibleId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f5de18be88682046cac6c4d4156f48fd3e4994d2e7b9ab1bbdc52f0a2e768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326748"
---
# <a name="aria-range-control-attributes-incompatible"></a>Inkompatible ARIA-Bereichssteuerelementattribute

## <a name="text"></a>Text

Das Element verfügt über **eine Progressbar-** oder **Schiebereglerrolle,** aber der verfügbar gemachte **aria-valuenow-Wert** liegt außerhalb des **Bereichs aria-valuemin** **aria-valuemax.**

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Dieser Fehler gilt für Elemente, die über eine [**Rolle**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implizit oder explizit) verfügen, die der **Statusleiste,** dem **Schieberegler** oder dem **Drehfeld entspricht.**

Dieser Fehler gibt an, dass sich der verfügbar gemachte [**aria-valuenow-Wert**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) nicht im Bereich befindet, der durch die Attribute [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) und [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) definiert wird.

Um diesen Fehler zu beheben, überprüfen Sie Ihre Implementierung, um sicherzustellen, dass die Attribute [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) und [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) richtig festgelegt sind und dass der [**aria-valuenow-Attributwert**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) ordnungsgemäß beibehalten wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ARIA-Bereichssteuerelementattribute fehlen](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




