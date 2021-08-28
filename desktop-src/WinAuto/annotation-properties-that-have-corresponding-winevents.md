---
title: Anmerkungseigenschaften mit entsprechenden WinEvents
description: Seien Sie vorsichtig, wenn Sie Eigenschaften überschreiben, die sich häufig ändern, insbesondere solche, die von Clients als Ergebnis eines WinEvent untersucht werden (z. B. Zustand, Wert und bei einigen Steuerelementen die Eigenschaften Name).
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753a17498daf9966ed1c3dfa98dc64fbdb2290011842c4fe9c194f50bf408ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098510"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a>Anmerkungseigenschaften mit entsprechenden WinEvents

Seien Sie vorsichtig, wenn Sie Eigenschaften überschreiben, die sich häufig ändern, insbesondere solche, die von Clients als Ergebnis eines WinEvent untersucht werden (z. B. [**State**](state-property.md), [**Value**](value-property.md)und bei einigen Steuerelementen die [**Name-Eigenschaften).**](name-property.md)

In vielen Fällen, insbesondere bei USER- und ComCtl-Steuerelementen, wird das WinEvent, das eine Eigenschaftsänderung signalisiert, gesendet, bevor der Besitzer des Steuerelements benachrichtigt wird (in der Regel über [WM \_ NOTIFY](../controls/wm-notify.md)). Das Aktualisieren der Eigenschaft [**mit SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) im WM NOTIFY-Handler ist zu spät. Clients, die kontextspezifische Hooks verwenden, haben bereits auf \_ den alten Wert zugegriffen.

Sie können diese Eigenschaftentypen mithilfe von Rückrufserverobjekten behandeln (mit [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); Der Server kann jedoch keinen Zustand verwenden, der im WM NOTIFY-Handler aktualisiert wird, da dieser Handler \_ noch nicht aufgerufen wurde. Anstatt beispielsweise eine zwischengespeicherte aktuelle Wertvariable zu verwenden, die im WM NOTIFY-Handler aktualisiert wird und veraltet ist, sollte das \_ [**IAccPropServer::GetPropValue-Rückrufobjekt**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) eine Nachricht direkt an das Steuerelement senden, um seinen tatsächlichen aktuellen Wert zum Generieren der erforderlichen Eigenschaft zu erhalten.

 

 