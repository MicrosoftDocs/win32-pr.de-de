---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Bestimmt, ob ein angegebener [DXCoreAdapterPreference-Wert](./ne-dxcore_interface-dxcoreadapterpreference.md) vom Betriebssystem verstanden wird.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: f8a42040ecd6c5667a3d33fb506fd97cfdfe53e8950c2e42b6068bbed6c19467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502581"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a>IDXCoreAdapterList::IsAdapterPreferenceSupported-Methode

## <a name="description"></a>BESCHREIBUNG

Bestimmt, ob ein angegebener [DXCoreAdapterPreference-Wert](./ne-dxcore_interface-dxcoreadapterpreference.md) vom aktuellen Betriebssystem verstanden wird. Sie können **IsAdapterPreferenceSupported** aufrufen, bevor [Sie IDXCoreAdapterList::Sort aufrufen.](./nf-dxcore_interface-idxcoreadapterlist-sort.md)

## <a name="syntax"></a>Syntax

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a>Parameter

### <a name="preference"></a>Einstellung

Typ: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**

Ein [DXCoreAdapterPreference-Wert,](./ne-dxcore_interface-dxcoreadapterpreference.md) der überprüft wird, um festzustellen, ob er vom Betriebssystem unterstützt wird.

## <a name="returns"></a>Gibt zurück

Typ: **bool**

Gibt `true` zurück, wenn der Sortiertyp vom aktuellen Betriebssystem verstanden wird. Andernfalls wird `false`zurückgegeben.

## <a name="see-also"></a>Weitere Informationen

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)