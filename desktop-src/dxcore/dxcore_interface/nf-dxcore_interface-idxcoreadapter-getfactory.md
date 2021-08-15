---
title: IDXCoreAdapter::GetFactory
description: Ruft einen [IDXCoreAdapterFactory-Schnittstellenzeiger](./nn-dxcore_interface-idxcoreadapterfactory.md) auf das DXCore-Adapterfactoryobjekt ab. | IDXCoreAdapter::GetFactory
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 759960875f67acefabf9f4207a9ea38150757b0b2bbec673e6feed3b0c197ee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279463"
---
# <a name="idxcoreadaptergetfactory-method"></a>IDXCoreAdapter::GetFactory-Methode

Ruft einen [IDXCoreAdapterFactory-Schnittstellenzeiger](./nn-dxcore_interface-idxcoreadapterfactory.md) auf das DXCore-Adapterfactoryobjekt ab. Programmieranleitungen und Codebeispiele finden Sie unter [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)(Verwenden von DXCore zum Aufzählen von Adaptern).

## <a name="syntax"></a>Syntax

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory
) = 0;

template <class T>
HRESULT GetFactory(_COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a>Parameter

### <a name="riid"></a>riid

Typ: **REFIID**

Ein Verweis auf die GUID (Globally Unique Identifier) der Schnittstelle, die in *ppvFactory zurückgegeben werden soll.* Es wird erwartet, dass dies der Schnittstellenbezeichner (IID) von [IDXCoreAdapterFactory ist.](./nn-dxcore_interface-idxcoreadapterfactory.md)

### <a name="ppvfactory-out"></a>ppvFactory [out]

Typ: **\* \* void**

Die Adresse eines Zeigers auf eine Schnittstelle mit der IID, die im *riid-Parameter angegeben* ist. Nach erfolgreicher Rückgabe enthält *\* ppvFactory* (die dereferenzierte Adresse) einen Zeiger auf das vorhandene DXCore-Adapterfactoryobjekt. Vor der Rückgabe erhöht die Funktion den Verweiszähler für die [IDXCoreAdapterFactory-Schnittstelle](./nn-dxcore_interface-idxcoreadapterfactory.md) des Factoryobjekts.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ist, gibt **sie** S_OK. Andernfalls wird ein [**HRESULT-Fehlercode**](../../com/structure-of-com-error-codes.md) [zurückgegeben.](../../com/com-error-codes-10.md)

|Rückgabewert|Beschreibung|
|-|-|
|E_NOINTERFACE|Für riid wurde ein *ungültiger Wert angegeben.*|
|E_POINTER|`nullptr`wurde für *ppvFactory bereitgestellt.*|

## <a name="remarks"></a>Hinweise

Für die Dauer, für die ein Verweis auf einer [IDXCoreAdapterFactory-Schnittstelle,](./nn-dxcore_interface-idxcoreadapterfactory.md) einer [IDXCoreAdapterList-Schnittstelle](./nn-dxcore_interface-idxcoreadapterlist.md) oder einer [IDXCoreAdapter-Schnittstelle](./nn-dxcore_interface-idxcoreadapter.md) vorhanden ist, geben zusätzliche Aufrufe von [DXCoreCreateAdapterFactory,](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md) [IDXCoreAdapterList::GetFactory](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md)oder [IDXCoreAdapter::GetFactory]() Zeiger auf dasselbe Objekt zurück, was die Verweisanzahl der **IDXCoreAdapterFactory-Schnittstelle** erhöht.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)
