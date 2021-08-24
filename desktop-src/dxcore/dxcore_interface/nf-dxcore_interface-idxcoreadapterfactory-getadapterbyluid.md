---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Ruft das DXCore-Adapterobjekt ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) für eine angegebene LUID ab, falls verfügbar.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: d8f72aba23b9a1f57094b39e5afba3740f8749348c6a2da6a8753f72a7a0e6ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787051"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a>IDXCoreAdapterFactory::GetAdapterByLuid-Methode

Ruft das DXCore-Adapterobjekt ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) für eine angegebene LUID ab, falls verfügbar. Programmieranleitungen und Codebeispiele finden Sie unter [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)(Verwenden von DXCore zum Aufzählen von Adaptern).

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

### <a name="adapterluid"></a>adapterLUID

Typ: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**

Der lokal eindeutige Wert, der die Adapterinstanz identifiziert.

### <a name="riid-in"></a>riid [in]

Typ: **REFIID**

Ein Verweis auf die GUID (Globally Unique Identifier) der Schnittstelle, die in *ppvAdapter zurückgegeben werden soll.* Es wird erwartet, dass dies der Schnittstellenbezeichner (IID) von [IDXCoreAdapter ist.](./nn-dxcore_interface-idxcoreadapter.md)

### <a name="ppvadapter-out"></a>ppvAdapter [out]

Typ: **\* \* void**

Die Adresse eines Zeigers auf eine Schnittstelle mit der IID, die im *riid-Parameter angegeben* ist. Nach erfolgreicher Rückgabe enthält *\* ppvAdapter* (die dereferenzierte Adresse) einen Zeiger auf den erstellten DXCore-Adapter.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ist, gibt **sie** S_OK. Andernfalls wird ein [**HRESULT-Fehlercode**](../../com/structure-of-com-error-codes.md) [zurückgegeben.](../../com/com-error-codes-10.md)

|Rückgabewert|Beschreibung|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|Die in adapterLUID übergebene *Adapter-LUID* wird erkannt, aber der Adapter befindet sich nicht mehr in einem gültigen Zustand.|
|E_INVALIDARG|Es ist keine solche Adapter-LUID verfügbar, da der in *adapterLUID* übergebene Wert über DXCore verfügbar ist.|
|E_NOINTERFACE|Für riid wurde ein *ungültiger Wert angegeben.*|
|E_POINTER|`nullptr`wurde für *ppvAdapter bereitgestellt.*|

## <a name="remarks"></a>Hinweise

Mehrere Aufrufe, die dieselbe [LUID übergeben,](/windows/win32/api/winnt/ns-winnt-luid) geben identische Schnittstellenzeige zurück. Daher ist es sicher, Schnittstellenzeker zu vergleichen, um zu bestimmen, ob mehrere Zeiger auf das gleiche Adapterobjekt verweisen.

## <a name="see-also"></a>Weitere Informationen

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore-Referenz](../dxcore-reference.md), Verwenden von DXCore zum [Aufzählen von Adaptern](../dxcore-enum-adapters.md)