---
title: IDXCoreAdapter::IsValid
description: Bestimmt, ob dieses DXCore-Adapterobjekt noch gültig ist.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6b8a0ccadb46f20db9c5f2a23ac8709b391254ee453f05424dadee309f33fc40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842540"
---
# <a name="idxcoreadapterisvalid-method"></a>IDXCoreAdapter::IsValid-Methode

Bestimmt, ob dieses DXCore-Adapterobjekt noch gültig ist. Programmieranleitungen und Codebeispiele finden Sie unter [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)(Verwenden von DXCore zum Aufzählen von Adaptern).

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a>Rückgabe

Typ: **bool**

Gibt `true` zurück, wenn dieses DXCore-Adapterobjekt noch gültig ist. Andernfalls wird `false`zurückgegeben.

## <a name="see-also"></a>Weitere Informationen

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)