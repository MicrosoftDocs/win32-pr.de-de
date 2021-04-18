---
title: IDXCoreAdapter::SetState
description: Legt den Zustand des angegebenen Elements auf dem Adapter fest.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8cbeacdb8c6020441b5dd74a9f9233a6c112b4f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340729"
---
# <a name="idxcoreadaptersetstate-method"></a>Idxcoreadapter:: SetState-Methode

Legt den Zustand des angegebenen Elements auf dem Adapter fest. Bevor Sie **SetState** für einen Eigenschaftentyp aufrufen, rufen Sie [issetstaatupportiert](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) auf, um zu bestätigen, dass das Festlegen der Statusart für diesen Adapter und das Betriebssystem (OS) verfügbar ist.

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

Typ: **[dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md)**

Die Art des Zustands Elements auf dem Adapter, dessen Zustand Sie festlegen möchten. Weitere Informationen zu den einzelnen adapterstatusarten finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .

### <a name="inputstatedetailssize"></a>Input statedetailssize

Typ: **size_t**

Die Größe (in Bytes) des Eingangs Zustands Details-Puffers, den Sie (optional) zuordnen und in *inputstatedetails* angeben können.

### <a name="inputstatedetails-in"></a>Input statedetails [in]

Typ: **void konstant \***

Ein optionaler Zeiger auf einen konstanten Eingabe Zustands Details-Puffer, den Sie in der Anwendung zuordnen, der alle Informationen zu Ihrer Anforderung enthält, die für die im *Status* angegebene Zustands Angabe erforderlich sind. Weitere Informationen zu allen Eingabepuffer Anforderungen für eine bestimmte Statusart finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .

### <a name="inputdatasize"></a>inputdatasize

Typ: **size_t**

Die Größe (in Bytes) des Eingabe Puffers, den Sie zuordnen und in *inputData* bereitstellen.

### <a name="inputdata-in"></a>Input Data [in]

Typ: **void \***

Ein Zeiger auf einen Eingabepuffer, den Sie in der Anwendung zuordnen, mit den Zustandsinformationen, die für das Zustands Element festgelegt werden, dessen Art Sie im *Zustand* angeben. Weitere Informationen zu den Eingabepuffer Anforderungen für eine bestimmte Art von Zustand finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|Der Adapter befindet sich nicht mehr in einem gültigen Zustand.|
|DXGI_ERROR_INVALID_CALL|Die im *Status* angegebene Zustands Angabe wird von diesem Betriebssystem (OS) nicht erkannt. Wenden Sie sich an [issetstaatupportiert](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) , um zu bestätigen, dass das Festlegen der Zustands Art für diesen Adapter und das Betriebssystem (OS) verfügbar ist.|
|DXGI_ERROR_UNSUPPORTED|Die im *Status* angegebene Statusart wird vom Adapter nicht unterstützt. Wenden Sie sich an [issetstaatupportiert](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) , um zu bestätigen, dass das Festlegen der Zustands Art für diesen Adapter und das Betriebssystem (OS) verfügbar ist.|
|E_INVALIDARG|Für *inputData* (oder für *inputstatedetails* , bei denen ein Eingabe Zustands Details-Puffer erforderlich ist) ist eine unzureichende Puffergröße angegeben.|
|E_POINTER|`nullptr` wurde für *inputData* bereitgestellt (oder für *inputstatedetails* , wenn ein Eingabe Zustands Details-Puffer erforderlich ist).|

## <a name="see-also"></a>Siehe auch

[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)