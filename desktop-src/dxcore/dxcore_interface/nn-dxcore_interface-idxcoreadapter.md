---
title: IDXCoreAdapter
description: Die **idxcoreadapter**-   Schnittstelle implementiert Methoden zum Abrufen von Details zu einem Adapter Element.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0930ce76353d556f7839f476ec8979823eac3a6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102194"
---
# <a name="idxcoreadapter-interface"></a>Idxcoreadapter-Schnittstelle

Die **idxcoreadapter**-   Schnittstelle implementiert Methoden zum Abrufen von Details zu einem Adapter Element. **Idxcoreadapter** erbt von der [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).

## <a name="remarks"></a>Bemerkungen

Die Eigenschaften eines Adapters werden zu dem Zeitpunkt eingerichtet, zu dem der Adapter startet, und sind für die Lebensdauer des Adapters unveränderlich. Dies steht im Gegensatz zum Zustand eines Adapters, der abgefragt oder festgelegt werden kann, und die Werte von, die sich im Laufe der Zeit ändern können.

## <a name="see-also"></a>Siehe auch

[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)