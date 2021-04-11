---
title: IDXCoreAdapter::GetProperty
description: Ruft den Wert der angegebenen Adapter Eigenschaft ab.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c8a7f7b36fdb0128b4047335051823da07a074c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316262"
---
# <a name="idxcoreadaptergetproperty-method"></a>Idxcoreadapter:: GetProperty-Methode

Ruft den Wert der angegebenen Adapter Eigenschaft ab. Bevor Sie **GetProperty** für einen Eigenschaftentyp aufrufen, rufen Sie [ispropertysupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) auf, um zu bestätigen, dass der Eigenschaftentyp für diesen Adapter und dieses Betriebssystem (OS) verfügbar ist. Rufen Sie auch vor dem Aufrufen von **GetProperty** [getpropertysize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) auf, um die erforderliche Größe des Puffers zu bestimmen, in dem der Eigenschafts Wert empfangen werden soll.

## <a name="syntax"></a>Syntax

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a>Parameter

### <a name="property"></a>property

Type: **[dxcoreadapterproperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Der Typ der Eigenschaft, deren Wert abgerufen werden soll. Weitere Informationen zu den einzelnen Adapter Eigenschaften finden Sie in der Tabelle unter [dxcoreadapterproperty](./ne-dxcore_interface-dxcoreadapterproperty.md) .

### <a name="buffersize"></a>bufferSize

Typ: **size_t**

Die Größe (in Bytes) des Ausgabepuffers, den Sie zuordnen und in *PropertyData* bereitstellen.

### <a name="propertydata-out"></a>PropertyData [out]

Typ: **void \***

Ein Zeiger auf einen Ausgabepuffer, den Sie in der Anwendung zuordnen, und der die Funktion ausfüllt. Ruft [getpropertysize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) auf, um die Größe zu ermitteln, die der *PropertyData* -Puffer für eine bestimmte Adapter Eigenschaft aufweisen soll.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|DXGI_ERROR_INVALID_CALL|Der in der- *Eigenschaft* angegebene Eigenschaftentyp wird von diesem Betriebssystem (OS) nicht erkannt. Wenden Sie [ispropertysupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) an, um zu bestätigen, dass der Eigenschaftentyp für diesen Adapter und dieses Betriebssystem verfügbar ist.|
|DXGI_ERROR_UNSUPPORTED|Der in der- *Eigenschaft* angegebene Eigenschaftentyp wird vom Adapter nicht unterstützt. Wenden Sie [ispropertysupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) an, um zu bestätigen, dass der Eigenschaftentyp für diesen Adapter und dieses Betriebssystem verfügbar ist.|
|E_INVALIDARG|In *PropertyData* ist eine unzureichende Puffergröße angegeben. Ruft [getpropertysize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) auf, um die Größe zu ermitteln, die der *PropertyData* -Puffer für eine bestimmte Adapter Eigenschaft aufweisen soll.|
|E_POINTER|`nullptr` wurde für *PropertyData* bereitgestellt.|

## <a name="remarks"></a>Bemerkungen

Sie können **GetProperty** für einen Adapter aufrufen, der nicht mehr gültig ist, &mdash; da die Funktion nicht mehr gültig ist. Diese Funktion gibt den *PropertyData* -Puffer aus, bevor Sie aufgefüllt wird.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)