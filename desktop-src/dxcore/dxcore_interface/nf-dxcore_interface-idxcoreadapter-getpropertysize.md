---
title: IDXCoreAdapter::GetPropertySize
description: Ruft für eine angegebene Adaptereigenschaft die Größe des Puffers in Bytes ab, die für einen Aufruf von [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)erforderlich ist.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 525e2657ab7af5fa6f7cee4f527b74604d2674dbc67da232dd6501ddc45b0291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279252"
---
# <a name="idxcoreadaptergetpropertysize-method"></a>IDXCoreAdapter::GetPropertySize-Methode

Ruft für eine angegebene Adaptereigenschaft die Größe des Puffers in Bytes ab, die für einen Aufruf von [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)erforderlich ist. Rufen Sie vor dem Aufrufen von **GetPropertySize** für einen Eigenschaftentyp [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) auf, um zu bestätigen, dass der Eigenschaftstyp für diesen Adapter und das Betriebssystem verfügbar ist.

## <a name="syntax"></a>Syntax

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a>Parameter

### <a name="property"></a>property

Typ: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Der Typ der Eigenschaft, deren Größe Sie in Bytes abrufen möchten.

### <a name="buffersize-out"></a>bufferSize [out]

Typ: **size_t \***

Ein Zeiger auf einen **size_t** Wert. Die Funktion dereferenziert den Zeiger und legt den Wert auf die Größe des Ausgabepuffers in Bytes fest, den Sie im Aufruf von [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)als *propertyData-Argument* zuweisen und übergeben sollten.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](../../com/structure-of-com-error-codes.md) [](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|Beschreibung|
|-|-|
|DXGI_ERROR_INVALID_CALL|Der in *der -Eigenschaft* angegebene Eigenschaftentyp wird von diesem Betriebssystem (Betriebssystem) nicht erkannt. Rufen Sie [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) auf, um zu bestätigen, dass der Eigenschaftstyp für diesen Adapter und das Betriebssystem verfügbar ist.|
|DXGI_ERROR_UNSUPPORTED|Der in *der -Eigenschaft* angegebene Eigenschaftentyp wird vom Adapter nicht unterstützt. Rufen Sie [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) auf, um zu bestätigen, dass der Eigenschaftstyp für diesen Adapter und das Betriebssystem verfügbar ist.|
|E_POINTER|`nullptr` wurde für *bufferSize* bereitgestellt.|

## <a name="remarks"></a>Hinweise

Sie können **GetPropertySize** auf einem Adapter aufrufen, der nicht mehr gültig ist. Die &mdash; Funktion schlägt nicht fehl.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)