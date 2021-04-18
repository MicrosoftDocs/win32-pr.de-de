---
title: IDXCoreAdapterList::IsStale
description: Bestimmt, ob Änderungen an diesem System dazu geführt haben, dass dieses DXCore-Adapter Listen Objekt veraltet geworden ist.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68b4e4ba6f3434f76ea5b4a2a98ae4e83486f61e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340527"
---
# <a name="idxcoreadapterlistisstale-method"></a>Idxcoreadapterlist:: isstale-Methode

Bestimmt, ob Änderungen an diesem System dazu geführt haben, dass dieses DXCore-Adapter Listen Objekt veraltet geworden ist. Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a>Gibt zurück

Typ: **bool**

Gibt zurück,  `true`   Wenn bei der Erstellung der Liste Änderungen an den Systembedingungen aufgetreten sind, die dazu geführt haben, dass diese Adapter Liste veraltet ist. Andernfalls wird zurückgegeben  `false` .

## <a name="remarks"></a>Bemerkungen

Sie können " **isstale** " Abfragen, um zu bestimmen, ob eine Änderung der Systembedingungen dazu geführt hat, dass diese Liste veraltet ist. Wenn **isstale** einmal zurückgibt `true` , wird `true` für die verbleibende Lebensdauer des DXCore-Adapter Listen Objekts zurückgegeben. Ein veraltetes Listen Objekt wird weiterhin als veraltet eingestuft, auch wenn die Systembedingungen zu einem Status zurückkehren, der der Liste entspricht (die gleichen Bedingungen werden nun wie bei der ersten Generierung der Liste abgerufen).

## <a name="see-also"></a>Siehe auch

[Idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)