---
title: IDXCoreAdapter::QueryState
description: Ruft den aktuellen Zustand des angegebenen Elements auf dem Adapter ab.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 61fc5c601904011de8f343777a95385a16ec3d7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338283"
---
# <a name="idxcoreadapterquerystate-method"></a>Idxcoreadapter:: querystate-Methode

Ruft den aktuellen Zustand des angegebenen Elements auf dem Adapter ab. Rufen Sie vor dem Aufrufen von **querystate** für einen Eigenschaftentyp [isquerystaatupportiert](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) auf, um zu bestätigen, dass für diesen Adapter und dieses Betriebssystem eine Abfrage der Art des Zustands verfügbar ist.

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

Typ: **[dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md)**

Die Art des Zustands Elements auf dem Adapter, dessen Zustand Sie abrufen möchten. Weitere Informationen zu den einzelnen adapterstatusarten finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .

### <a name="inputstatedetailssize"></a>Input statedetailssize

Typ: **size_t**

Die Größe (in Bytes) des Eingangs Zustands Details-Puffers, den Sie (optional) zuordnen und in *inputstatedetails* angeben können.

### <a name="inputstatedetails-in"></a>Input statedetails [in]

Typ: **void konstant \***

Ein optionaler Zeiger auf einen konstanten Eingabe Zustands Details-Puffer, den Sie in der Anwendung zuordnen, der alle Informationen zu Ihrer Anforderung enthält, die für die im *Status* angegebene Zustands Angabe erforderlich sind. Weitere Informationen zu allen Eingabepuffer Anforderungen für eine bestimmte Statusart finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .

### <a name="outputbuffersize"></a>outputbuffersize

Typ: **size_t**

Die Größe (in Bytes) des Ausgabepuffers, den Sie zuordnen und in *OUTPUTBUFFER* bereitstellen.

### <a name="outputbuffer-out"></a>OUTPUTBUFFER [out]

Typ: **void \***

Ein Zeiger auf einen Ausgabepuffer, den Sie in der Anwendung zuordnen, und der die Funktion ausfüllt. Weitere Informationen zu den Anforderungen des Ausgabepuffers für eine bestimmte Art von Zustand finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|Der Adapter befindet sich nicht mehr in einem gültigen Zustand.|
|DXGI_ERROR_INVALID_CALL|Die im *Status* angegebene Zustands Angabe wird von diesem Betriebssystem (OS) nicht erkannt. Wenden Sie sich an [isquerystaatupportiert](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) , um zu bestätigen, dass für diesen Adapter und dieses Betriebssystem eine Abfrage der Art des Zustands verfügbar ist.|
|DXGI_ERROR_UNSUPPORTED|Die im *Status* angegebene Statusart wird vom Adapter nicht unterstützt. Wenden Sie sich an [isquerystaatupportiert](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) , um zu bestätigen, dass für diesen Adapter und dieses Betriebssystem eine Abfrage der Art des Zustands verfügbar ist.|
|E_INVALIDARG|Eine unzureichende Puffergröße wird für *OUTPUTBUFFER* bereitgestellt (oder für input *statedetails* , wenn ein Eingabe Zustands Details-Puffer erforderlich ist).|
|E_POINTER|`nullptr` wurde für *OUTPUTBUFFER* bereitgestellt (oder für *inputstatedetails* , wenn ein Eingabe Zustands Details-Puffer erforderlich ist).|

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu den einzelnen adapterstatusart und den verwendeten Eingaben und Ausgaben finden Sie unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) . Diese Funktion gibt den *OUTPUTBUFFER* -Puffer aus, bevor Sie aufgefüllt wird.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)