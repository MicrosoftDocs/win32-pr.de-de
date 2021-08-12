---
title: IDXCoreAdapter
description: Die **IDXCoreAdapter-Schnittstelle** implementiert Methoden zum Abrufen von Details zu einem Adapterelement.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 18cdd8082701ea4f1a8b5a3cfa047decd0f77df81b17eebe49bf5a8a887663fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278787"
---
# <a name="idxcoreadapter-interface"></a>IDXCoreAdapter-Schnittstelle

Die **IDXCoreAdapter-Schnittstelle** implementiert Methoden zum Abrufen von Details zu einem Adapterelement. **IDXCoreAdapter** erbt von der [IUnknown-Schnittstelle.](/windows/win32/api/unknwn/nn-unknwn-iunknown) Programmieranleitungen und Codebeispiele finden Sie unter [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)(Verwenden von DXCore zum Aufzählen von Adaptern).

## <a name="remarks"></a>Hinweise

Die Eigenschaften eines Adapters werden beim Start des Adapters festgelegt und sind für die Lebensdauer des Adapters unveränderlich. Dies steht im Gegensatz zum Zustand eines Adapters, der abgefragt oder festgelegt werden kann und dessen Werte sich im Laufe der Zeit ändern können.

## <a name="see-also"></a>Siehe auch

[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)