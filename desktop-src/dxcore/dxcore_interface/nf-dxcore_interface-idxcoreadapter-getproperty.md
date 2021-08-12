---
title: IDXCoreAdapter::GetProperty
description: Ruft den Wert der angegebenen Adaptereigenschaft ab.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8adb48994580125d153c36394c4db65cb38f4a08306814d1638e5c27eb3d4868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279400"
---
# <a name="idxcoreadaptergetproperty-method"></a>IDXCoreAdapter::GetProperty-Methode

Ruft den Wert der angegebenen Adaptereigenschaft ab. Rufen Sie vor dem Aufrufen von **GetProperty** für einen Eigenschaftentyp [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) auf, um zu bestätigen, dass der Eigenschaftstyp für diesen Adapter und das Betriebssystem verfügbar ist. Rufen Sie außerdem vor dem Aufrufen von **GetProperty** [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) auf, um die erforderliche Größe des Puffers zu bestimmen, in dem der Eigenschaftswert empfangen werden soll.

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

Typ: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Der Typ der Eigenschaft, deren Wert Sie abrufen möchten. Weitere Informationen zu den einzelnen Adaptereigenschaften finden Sie in der Tabelle in [DXCoreAdapterProperty.](./ne-dxcore_interface-dxcoreadapterproperty.md)

### <a name="buffersize"></a>bufferSize

Typ: **size_t**

Die Größe des Ausgabepuffers in Bytes, den Sie zuordnen und in *propertyData* bereitstellen.

### <a name="propertydata-out"></a>propertyData [out]

Typ: **\* void**

Ein Zeiger auf einen Ausgabepuffer, den Sie in Ihrer Anwendung zuordnen und den die Funktion ausfüllt. Rufen [Sie GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) auf, um die Größe zu bestimmen, die der *propertyData-Puffer* für eine bestimmte Adaptereigenschaft haben soll.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](../../com/structure-of-com-error-codes.md) [](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|Beschreibung|
|-|-|
|DXGI_ERROR_INVALID_CALL|Der in *der -Eigenschaft* angegebene Eigenschaftentyp wird von diesem Betriebssystem (Betriebssystem) nicht erkannt. Rufen Sie [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) auf, um zu bestätigen, dass der Eigenschaftstyp für diesen Adapter und das Betriebssystem verfügbar ist.|
|DXGI_ERROR_UNSUPPORTED|Der in *der -Eigenschaft* angegebene Eigenschaftentyp wird vom Adapter nicht unterstützt. Rufen Sie [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) auf, um zu bestätigen, dass der Eigenschaftstyp für diesen Adapter und das Betriebssystem verfügbar ist.|
|E_INVALIDARG|Eine unzureichende Puffergröße wird in *propertyData* bereitgestellt. Rufen [Sie GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) auf, um die Größe zu bestimmen, die der *propertyData-Puffer* für eine bestimmte Adaptereigenschaft haben soll.|
|E_POINTER|`nullptr` wurde für *propertyData* bereitgestellt.|

## <a name="remarks"></a>Hinweise

Sie können **GetProperty** für einen Adapter aufrufen, der nicht mehr gültig ist, da die Funktion dadurch &mdash; nicht fehlschlägt. Diese Funktion entfernt den *propertyData-Puffer* auf null, bevor er ausgefüllt wird.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)