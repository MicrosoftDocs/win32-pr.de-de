---
title: IDXCoreAdapterList::GetAdapter
description: Ruft einen bestimmten Adapter nach Index aus einem DXCore-Adapter Listen Objekt ab.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039417"
---
# <a name="idxcoreadapterlistgetadapter-method"></a>Idxcoreadapterlist:: GetAdapter-Methode

Ruft einen bestimmten Adapter nach Index aus einem DXCore-Adapter Listen Objekt ab. Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).

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

Ein NULL basierter Index, der eine Adapter Instanz innerhalb der DXCore-Adapter Liste identifiziert.

### <a name="riid"></a>riid

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
|DXGI_ERROR_DEVICE_REMOVED|Der *Index* ist gültig, aber der Adapter befindet sich nicht mehr in einem gültigen Zustand.|
|E_INVALIDARG|Der angegebene *Index* ist ungültig.|
|E_NOINTERFACE|Für *riid* wurde ein ungültiger Wert angegeben.|
|E_POINTER|`nullptr` wurde für *ppvadapter* bereitgestellt.|

## <a name="remarks"></a>Bemerkungen

Mehrere Aufrufe, die einen Index übergeben, der denselben Adapter darstellt, geben identische Schnittstellen Zeiger zurück, auch über verschiedene Adapter Listen hinweg. Daher ist es sicher, Schnittstellen Zeiger zu vergleichen, um zu bestimmen, ob mehrere Zeiger auf dasselbe Adapter Objekt verweisen.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)