---
title: IDXCoreAdapter::GetPropertySize
description: Ruft für eine angegebene Adapter Eigenschaft die Größe des Puffers in Bytes ab, der für den Abruf von [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)erforderlich ist.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340916"
---
# <a name="idxcoreadaptergetpropertysize-method"></a>Idxcoreadapter:: getpropertysize-Methode

Ruft für eine angegebene Adapter Eigenschaft die Größe des Puffers in Bytes ab, der für den Abruf von [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)erforderlich ist. Bevor Sie **getpropertysize** für einen Eigenschaftentyp aufrufen, rufen Sie [ispropertysupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) auf, um zu bestätigen, dass der Eigenschaftentyp für diesen Adapter und dieses Betriebssystem verfügbar ist.

## <a name="syntax"></a>Syntax

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a>Parameter

### <a name="property"></a>property

Type: **[dxcoreadapterproperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Der Typ der Eigenschaft, deren Größe (in Bytes) abgerufen werden soll.

### <a name="buffersize-out"></a>bufferSize [out]

Typ: **size_t \***

Ein Zeiger auf einen **size_t** Wert. Die Funktion dereferenziert den Zeiger und legt den Wert auf die Größe (in Bytes) des Ausgabepuffers fest, den Sie zuordnen und als *PropertyData* -Argument in Ihrem Aufrufen von [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)übergeben.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|DXGI_ERROR_INVALID_CALL|Der in der- *Eigenschaft* angegebene Eigenschaftentyp wird von diesem Betriebssystem (OS) nicht erkannt. Wenden Sie [ispropertysupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) an, um zu bestätigen, dass der Eigenschaftentyp für diesen Adapter und dieses Betriebssystem verfügbar ist.|
|DXGI_ERROR_UNSUPPORTED|Der in der- *Eigenschaft* angegebene Eigenschaftentyp wird vom Adapter nicht unterstützt. Wenden Sie [ispropertysupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) an, um zu bestätigen, dass der Eigenschaftentyp für diesen Adapter und dieses Betriebssystem verfügbar ist.|
|E_POINTER|`nullptr` wurde für *bufferSize* bereitgestellt.|

## <a name="remarks"></a>Bemerkungen

Sie können **getpropertysize** für einen Adapter aufrufen, der nicht mehr gültig ist, da &mdash; die Funktion nicht fehlschlägt.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)