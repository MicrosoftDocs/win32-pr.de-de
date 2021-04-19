---
title: IDXCoreAdapterList::GetFactory
description: 'Ruft einen [idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md) -Schnittstellen Zeiger auf das DXCore-adapterfactoryobjekt ab. | Idxcoreadapterlist:: GetFactory'
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 08dc93f5c7e086e33d15f666a2c5b94fd7dd7e58
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106371849"
---
# <a name="idxcoreadapterlistgetfactory-method"></a>Idxcoreadapterlist:: GetFactory-Methode

Ruft einen [idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md) -Schnittstellen Zeiger auf das DXCore-adapterfactoryobjekt ab. Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).

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

Typ: **refID**

Ein Verweis auf die Globally Unique Identifier (GUID) der Schnittstelle, die in *ppvfactory* zurückgegeben werden soll. Dies wird als Schnittstellen Bezeichner (IID) von [idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md)erwartet.

### <a name="ppvfactory-out"></a>ppvfactory [out]

Typ: **void \* \***

Die Adresse eines Zeigers auf eine Schnittstelle mit der im *riid* -Parameter angegebenen IID. Bei erfolgreicher Rückgabe enthält *\* ppvfactory* (die Dereferenzierte Adresse) einen Zeiger auf das vorhandene DXCore-adapterfactoryobjekt. Vor der Rückgabe erhöht die Funktion den Verweis Zähler für die [idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md) -Schnittstelle des Factory-Objekts.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|E_NOINTERFACE|Für *riid* wurde ein ungültiger Wert angegeben.|
|E_POINTER|`nullptr` wurde für *ppvfactory* bereitgestellt.|

## <a name="remarks"></a>Bemerkungen

Für den Zeitraum, in dem ein Verweis auf einer [idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md) -Schnittstelle vorhanden ist, eine [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md) -Schnittstelle oder eine [idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md) -Schnittstelle, zusätzliche Aufrufe von [dxcorecreateadapterfactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [idxcoreadapterlist:: GetFactory]()oder [idxcoreadapter:: GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) geben Zeiger auf dasselbe Objekt zurück und erhöhen den Verweis Zähler der **idxcoreadapterfactory** -Schnittstelle.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)
