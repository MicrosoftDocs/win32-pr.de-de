---
title: IDXCoreAdapter::QueryState
description: Ruft den aktuellen Zustand des angegebenen Elements auf dem Adapter ab.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2e5c585c249141c1491ddf36ee798d8b11148425026e9011bd0653169f998fb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117720"
---
# <a name="idxcoreadapterquerystate-method"></a>IDXCoreAdapter::QueryState-Methode

Ruft den aktuellen Zustand des angegebenen Elements auf dem Adapter ab. Rufen Sie vor dem Aufrufen von **QueryState** für einen Eigenschaftentyp [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) auf, um zu bestätigen, dass das Abfragen der Zustandsart für diesen Adapter und das Betriebssystem verfügbar ist.

## <a name="syntax"></a>Syntax

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a>Parameter

### <a name="state"></a>state

Typ: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

Die Art des Zustandselements auf dem Adapter, dessen Zustand Sie abrufen möchten. Weitere Informationen zu den einzelnen Adapterzustandsarten finden Sie in der Tabelle in [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md)

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

Typ: **size_t**

Die Größe des Eingabezustandsdetailspuffers in Bytes, den Sie (optional) zuordnen und in *inputStateDetails bereitstellen.*

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

Typ: **void \* const**

Ein optionaler Zeiger auf einen Puffer mit konstanten Eingabezustandsdetails, den Sie in Ihrer Anwendung zuordnen, der alle Informationen zu Ihrer Anforderung enthält, die für die Zustandsart erforderlich sind, die Sie im Zustand *angeben.* Weitere Informationen zu eingabepufferanforderungen für eine bestimmte Zustandsart finden Sie in der Tabelle in [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md)

### <a name="outputbuffersize"></a>outputBufferSize

Typ: **size_t**

Die Größe des Ausgabepuffers in Bytes, den Sie zuordnen und in *outputBuffer bereitstellen.*

### <a name="outputbuffer-out"></a>outputBuffer [out]

Typ: **\* void**

Ein Zeiger auf einen Ausgabepuffer, den Sie in Ihrer Anwendung zuordnen und den die Funktion ausfüllt. Weitere Informationen zur Ausgabepufferanforderung für eine bestimmte Zustandsart finden Sie in der Tabelle in [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md)

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ist, gibt **sie** S_OK. Andernfalls wird ein [**HRESULT-Fehlercode**](../../com/structure-of-com-error-codes.md) [zurückgegeben.](../../com/com-error-codes-10.md)

|Rückgabewert|Beschreibung|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|Der Adapter befindet sich nicht mehr in einem gültigen Zustand.|
|DXGI_ERROR_INVALID_CALL|Die im Zustand angegebene *Zustandsart* wird von diesem Betriebssystem nicht erkannt. Rufen [Sie IsQueryStateSupported auf,](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) um zu bestätigen, dass das Abfragen der Zustandsart für diesen Adapter und das Betriebssystem verfügbar ist.|
|DXGI_ERROR_UNSUPPORTED|Die im Zustand angegebene *Zustandsart* wird vom Adapter nicht unterstützt. Rufen [Sie IsQueryStateSupported auf,](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) um zu bestätigen, dass das Abfragen der Zustandsart für diesen Adapter und das Betriebssystem verfügbar ist.|
|E_INVALIDARG|Für *outputBuffer* wird eine unzureichende Puffergröße bereitgestellt (oder für *inputStateDetails,* bei denen ein Eingabezustandsdetails-Puffer erforderlich ist).|
|E_POINTER|`nullptr` wurde für *outputBuffer* bereitgestellt (oder für *inputStateDetails,* bei denen ein Eingabezustandsdetails-Puffer erforderlich ist).|

## <a name="remarks"></a>Hinweise

Unter [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) finden Sie weitere Informationen zu den einzelnen Adapterzustandsart und zu den verwendeten Ein- und Ausgaben. Diese Funktion 0 (null) gibt den *OutputBuffer-Puffer* aus, bevor er gefüllt wird.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)