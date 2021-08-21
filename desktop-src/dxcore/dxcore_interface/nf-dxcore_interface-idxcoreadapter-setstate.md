---
title: IDXCoreAdapter::SetState
description: Legt den Zustand des angegebenen Elements auf dem Adapter fest.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c80ca670be26ffdcefa5e89cee079d2225d204ee97e99e41f69686300a46230b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042908"
---
# <a name="idxcoreadaptersetstate-method"></a>IDXCoreAdapter::SetState-Methode

Legt den Zustand des angegebenen Elements auf dem Adapter fest. Rufen Sie vor dem Aufrufen von **SetState** für einen Eigenschaftstyp [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) auf, um zu bestätigen, dass das Festlegen der Zustandsart für diesen Adapter und das Betriebssystem verfügbar ist.

## <a name="syntax"></a>Syntax

```cpp
virtual HRESULT STDMETHODCALLTYPE SetState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t inputDataSize,
  _In_reads_bytes_(inputDataSize) const void *inputData) = 0;

template <class T1, class T2>
HRESULT SetState( 
  DXCoreAdapterState state,
  const T1 *inputStateDetails,
  const T2 *inputData);
```

## <a name="parameters"></a>Parameter

### <a name="state"></a>state

Typ: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

Die Art des Zustandselements auf dem Adapter, dessen Zustand Sie festlegen möchten. Weitere Informationen zu den einzelnen Zustandsart des Adapters finden Sie in der Tabelle in [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md)

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

Typ: **size_t**

Die Größe des Eingabezustandsdetailspuffers in Bytes, den Sie (optional) zuordnen und in *inputStateDetails* bereitstellen.

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

Typ: **void \* const**

Ein optionaler Zeiger auf einen konstanten Eingabezustandsdetailspuffer, den Sie in Ihrer Anwendung zuordnen, der alle Informationen zu Ihrer Anforderung enthält, die für die Zustandsart erforderlich sind, die Sie im *Zustand* angeben. Weitere Informationen zu Eingabepufferanforderungen für eine bestimmte Zustandsart finden Sie in der Tabelle in [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md)

### <a name="inputdatasize"></a>inputDataSize

Typ: **size_t**

Die Größe des Eingabepuffers in Bytes, den Sie in *inputData* zuordnen und bereitstellen.

### <a name="inputdata-in"></a>inputData [in]

Typ: **\* void**

Ein Zeiger auf einen Eingabepuffer, den Sie in Ihrer Anwendung zuordnen, der die Zustandsinformationen enthält, die für das Zustandselement festgelegt werden sollen, dessen Art Sie im *Zustand* angeben. Weitere Informationen zur Eingabepufferanforderung für eine bestimmte Zustandsart finden Sie in der Tabelle in [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md)

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](../../com/structure-of-com-error-codes.md) [](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|Beschreibung|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|Der Adapter befindet sich nicht mehr in einem gültigen Zustand.|
|DXGI_ERROR_INVALID_CALL|Die im *Zustand* angegebene Zustandsart wird von diesem Betriebssystem (Betriebssystem) nicht erkannt. Rufen Sie [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) auf, um zu bestätigen, dass das Festlegen der Zustandsart für diesen Adapter und das Betriebssystem verfügbar ist.|
|DXGI_ERROR_UNSUPPORTED|Die im *Zustand* angegebene Zustandsart wird vom Adapter nicht unterstützt. Rufen Sie [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) auf, um zu bestätigen, dass das Festlegen der Zustandsart für diesen Adapter und das Betriebssystem verfügbar ist.|
|E_INVALIDARG|Für *inputData* wird eine unzureichende Puffergröße bereitgestellt (oder für *inputStateDetails,* wo ein Puffer für Eingabezustandsdetails erforderlich ist).|
|E_POINTER|`nullptr` wurde für *inputData* bereitgestellt (oder für *inputStateDetails,* wo ein Puffer für Eingabezustandsdetails erforderlich ist).|

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)