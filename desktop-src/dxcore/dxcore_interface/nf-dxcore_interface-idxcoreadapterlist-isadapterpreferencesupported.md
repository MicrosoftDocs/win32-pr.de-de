---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Bestimmt, ob ein angegebener [dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md) -Wert vom Betriebssystem erkannt wird.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 1678568eb17c0dd833c130e6184931c8896261e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728040"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a>Idxcoreadapterlist:: isadapterpreferencesupportiert-Methode

## <a name="description"></a>BESCHREIBUNG

Bestimmt, ob ein angegebener [dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md) -Wert vom aktuellen Betriebssystem (OS) erkannt wird. Sie können **isadapterpreferencesupportiert** aufrufen, bevor Sie [idxcoreadapterlist:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md)aufrufen.

## <a name="syntax"></a>Syntax

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a>Parameter

### <a name="preference"></a>Einstellung

Typ: **[dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**

Ein [dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md) -Wert, der geprüft wird, um festzustellen, ob er vom Betriebssystem unterstützt wird.

## <a name="returns"></a>Gibt zurück

Typ: **bool**

Gibt zurück, `true` Wenn der Sortierungstyp vom aktuellen Betriebssystem erkannt wird. Andernfalls wird `false`zurückgegeben.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)