---
title: Annotation-Eigenschaften mit entsprechenden WinEvents
description: Seien Sie vorsichtig, wenn Sie Eigenschaften überschreiben, die sich häufig ändern, insbesondere diejenigen, die von Clients infolge eines WinEvent-Elements (z. b. Zustand, Wert und, bei manchen Steuerelementen, die namens Eigenschaften) überprüft werden.
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a8849c66cb0067b63be1c846e9e140ae06f4b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390565"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a>Annotation-Eigenschaften mit entsprechenden WinEvents

Seien Sie vorsichtig, wenn Sie Eigenschaften überschreiben, die sich häufig ändern, insbesondere diejenigen, die von Clients infolge eines WinEvent-Elements (z. b. [**Zustand**](state-property.md), [**Wert**](value-property.md)und, bei manchen Steuerelementen, die [**namens**](name-property.md) Eigenschaften) überprüft werden.

In vielen Fällen, insbesondere bei Benutzer-und COMCTL-Steuerelementen, wird das WinEvent, das eine Eigenschafts Änderung signalisiert, gesendet, bevor der Besitzer des Steuer Elements benachrichtigt wird (in der Regel über [WM \_ Notify](../controls/wm-notify.md)). Das Aktualisieren der Eigenschaft mithilfe von [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) im WM- \_ Benachrichtigungs Handler ist zu spät; Clients, die in-context-Verknüpfungen verwenden, haben bereits auf den alten Wert zugegriffen.

Sie können diese Eigenschaften Typen mithilfe von Rückruf Server Objekten (mit [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)) verarbeiten. der Server kann jedoch keinen Zustand verwenden, der im WM- \_ Benachrichtigungs Handler aktualisiert wird, da dieser Handler noch nicht aufgerufen wurde. Anstatt z. b. eine zwischengespeicherte Variable für den aktuellen Wert zu verwenden, die im WM \_ -Benachrichtigungs Handler aktualisiert wird und veraltet ist, sollte das [**IAccPropServer:: GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) -Rückruf Objekt eine Nachricht direkt an das-Steuerelement senden, um den tatsächlichen aktuellen Wert zu erhalten, um die erforderliche Eigenschaft zu generieren.

 

 