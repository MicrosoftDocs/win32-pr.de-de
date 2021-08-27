---
title: IDXCoreAdapterList::GetAdapter
description: Ruft einen bestimmten Adapter nach Index aus einem DXCore-Adapterlistenobjekt ab.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 96b2973e36c93ca50db273fc28bd0f02cbaf7a48f96e6833af7f14323c7de57d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022130"
---
# <a name="idxcoreadapterlistgetadapter-method"></a>IDXCoreAdapterList::GetAdapter-Methode

Ruft einen bestimmten Adapter nach Index aus einem DXCore-Adapterlistenobjekt ab. Programmierleitfäden und Codebeispiele finden Sie unter [Verwenden von DXCore zum Aufzählen von Adaptern.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Syntax

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>Parameter

### <a name="index"></a>Index

Typ: **uint32_t**

Ein nullbasierter Index, der eine Adapterinstanz in der DXCore-Adapterliste identifiziert.

### <a name="riid"></a>riid

Typ: **REFIID**

Ein Verweis auf die GUID (Globally Unique Identifier) der Schnittstelle, die in *ppvAdapter* zurückgegeben werden soll. Es wird erwartet, dass dies der Schnittstellenbezeichner (IID) von [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)ist.

### <a name="ppvadapter-out"></a>ppvAdapter [out]

Typ: **\* \* void**

Die Adresse eines Zeigers auf eine Schnittstelle mit der im *riid-Parameter* angegebenen IID. Nach erfolgreicher Rückgabe enthält *\* ppvAdapter* (die dereferenzierte Adresse) einen Zeiger auf den erstellten DXCore-Adapter.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](../../com/structure-of-com-error-codes.md) [](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|Der *Index* ist gültig, aber der Adapter befindet sich nicht mehr in einem gültigen Zustand.|
|E_INVALIDARG|Der angegebene *Index* ist ungültig.|
|E_NOINTERFACE|Für *riid* wurde ein ungültiger Wert bereitgestellt.|
|E_POINTER|`nullptr` wurde für *ppvAdapter* bereitgestellt.|

## <a name="remarks"></a>Hinweise

Mehrere Aufrufe, die einen Index übergeben, der denselben Adapter darstellt, geben identische Schnittstellenzeiger zurück, auch über verschiedene Adapterlisten hinweg. Daher ist es sicher, Schnittstellenzeiger zu vergleichen, um zu bestimmen, ob mehrere Zeiger auf dasselbe Adapterobjekt verweisen.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)