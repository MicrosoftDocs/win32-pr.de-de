---
title: IDXCoreAdapterList::GetAdapterCount
description: Ruft die Anzahl der Adapter in einem DXCore-Adapterlistenobjekt ab.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 952120a039e4060a45f5e6e1de607fd68b50fcd7d7cd88ce5a98474f8f2dcfdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985120"
---
# <a name="idxcoreadapterlistgetadaptercount-method"></a>IDXCoreAdapterList::GetAdapterCount-Methode

Ruft die Anzahl der Adapter in einem DXCore-Adapterlistenobjekt ab. Programmieranleitungen und Codebeispiele finden Sie unter [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)(Verwenden von DXCore zum Aufzählen von Adaptern).

## <a name="syntax"></a>Syntax

```cpp
virtual uint32_t STDMETHODCALLTYPE GetAdapterCount() = 0;
```

## <a name="returns"></a>Rückgabe

Typ: **uint32_t**

Gibt die Anzahl der Adapterelemente in der Liste zurück.

## <a name="see-also"></a>Weitere Informationen

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), Verwenden von DXCore zum [Auflisten von Adaptern](../dxcore-enum-adapters.md)