---
title: IDXCoreAdapterList::GetFactory
description: Ruft einen [IDXCoreAdapterFactory-Schnittstellenzeiger](./nn-dxcore_interface-idxcoreadapterfactory.md) auf das DXCore-Adapterfactoryobjekt ab. | IDXCoreAdapterList::GetFactory
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 97ae5ef0ba321dafaabf1813d943b738f5af4c586050b91712bf9ad93005cb35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094580"
---
# <a name="idxcoreadapterlistgetfactory-method"></a>IDXCoreAdapterList::GetFactory-Methode

Ruft einen [IDXCoreAdapterFactory-Schnittstellenzeiger](./nn-dxcore_interface-idxcoreadapterfactory.md) auf das DXCore-Adapterfactoryobjekt ab. Programmierleitfäden und Codebeispiele finden Sie unter [Verwenden von DXCore zum Aufzählen von Adaptern.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Syntax

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory) = 0;

template <class T>
HRESULT GetFactory(
  _COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a>Parameter

### <a name="riid"></a>riid

Typ: **REFIID**

Ein Verweis auf die GUID (Globally Unique Identifier) der Schnittstelle, die in *ppvFactory* zurückgegeben werden soll. Es wird erwartet, dass dies der Schnittstellenbezeichner (IID) von [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md)ist.

### <a name="ppvfactory-out"></a>ppvFactory [out]

Typ: **\* \* void**

Die Adresse eines Zeigers auf eine Schnittstelle mit der im *riid-Parameter* angegebenen IID. Nach erfolgreicher Rückgabe enthält *\* ppvFactory* (die dereferenzierte Adresse) einen Zeiger auf das vorhandene DXCore-Adapterfactoryobjekt. Vor der Rückgabe erhöht die Funktion den Verweiszähler für die [IDXCoreAdapterFactory-Schnittstelle](./nn-dxcore_interface-idxcoreadapterfactory.md) des Factoryobjekts.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](../../com/structure-of-com-error-codes.md) [](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|E_NOINTERFACE|Für *riid* wurde ein ungültiger Wert bereitgestellt.|
|E_POINTER|`nullptr` wurde für *ppvFactory* bereitgestellt.|

## <a name="remarks"></a>Hinweise

Für den Zeitraum, in dem ein Verweis auf eine [IDXCoreAdapterFactory-Schnittstelle,](./nn-dxcore_interface-idxcoreadapterfactory.md) eine [IDXCoreAdapterList-Schnittstelle](./nn-dxcore_interface-idxcoreadapterlist.md) oder eine [IDXCoreAdapter-Schnittstelle](./nn-dxcore_interface-idxcoreadapter.md) vorhanden ist, geben zusätzliche Aufrufe von [DXCoreCreateAdapterFactory,](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md) [IDXCoreAdapterList::GetFactory]()oder [IDXCoreAdapter::GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) Zeiger auf dasselbe Objekt zurück, wodurch die Verweisanzahl der **IDXCoreAdapterFactory-Schnittstelle** erhöht wird.

## <a name="see-also"></a>Weitere Informationen

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)
