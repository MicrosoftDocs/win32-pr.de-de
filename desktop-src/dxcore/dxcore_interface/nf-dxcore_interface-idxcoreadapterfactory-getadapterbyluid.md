---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Ruft das DXCore-Adapter Objekt ([idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md)) für eine angegebene LUID ab, falls verfügbar.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 30835948978e5c7f3f11f903322e4fa41f71d210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390742"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a>Idxcoreadapterfactory:: getadapterbyluid-Methode

Ruft das DXCore-Adapter Objekt ([idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md)) für eine angegebene LUID ab, falls verfügbar. Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntax

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>Parameter

### <a name="adapterluid"></a>adapterluid

Typ: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) -Konstante\&**

Der lokal eindeutige Wert, der die Adapter Instanz identifiziert.

### <a name="riid-in"></a>riid [in]

Typ: **refID**

Ein Verweis auf die Globally Unique Identifier (GUID) der Schnittstelle, die in *ppvadapter* zurückgegeben werden soll. Dies wird als Schnittstellen Bezeichner (IID) von [idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md)erwartet.

### <a name="ppvadapter-out"></a>ppvadapter [out]

Typ: **void \* \***

Die Adresse eines Zeigers auf eine Schnittstelle mit der im *riid* -Parameter angegebenen IID. Bei erfolgreicher Rückgabe enthält *\* ppvadapter* (die Dereferenzierte Adresse) einen Zeiger auf den erstellten DXCore-Adapter.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|Die in *adapterluid* weiter gegebene Adapter-LUID wird erkannt, aber der Adapter befindet sich nicht mehr in einem gültigen Zustand.|
|E_INVALIDARG|Keine solche Adapter-LUID, da der in *adapterluid* über gegebene Wert über DXCore verfügbar ist.|
|E_NOINTERFACE|Für *riid* wurde ein ungültiger Wert angegeben.|
|E_POINTER|`nullptr` wurde für *ppvadapter* bereitgestellt.|

## <a name="remarks"></a>Bemerkungen

Mehrere Aufrufe, die dieselbe [LUID](/windows/win32/api/winnt/ns-winnt-luid) übergeben, geben identische Schnittstellen Zeiger zurück. Daher ist es sicher, Schnittstellen Zeiger zu vergleichen, um zu bestimmen, ob mehrere Zeiger auf dasselbe Adapter Objekt verweisen.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)