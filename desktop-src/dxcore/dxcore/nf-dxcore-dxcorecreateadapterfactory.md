---
title: DXCoreCreateAdapterFactory
description: Erstellt eine DXCore-Adapterfactory, mit der Sie weitere DXCore-Objekte generieren können.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 90567d732f6febc5d95b460b2ff88929dd12b2f22275de9db0d6bc5f88ef99ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985180"
---
# <a name="dxcorecreateadapterfactory-function"></a>DXCoreCreateAdapterFactory-Funktion

## <a name="description"></a>BESCHREIBUNG

Erstellt eine DXCore-Adapterfactory, mit der Sie weitere DXCore-Objekte generieren können. Programmierleitfäden und Codebeispiele finden Sie unter [Verwenden von DXCore zum Aufzählen von Adaptern.](../dxcore-enum-adapters.md)

## <a name="parameters"></a>Parameter

### <a name="riid"></a>riid

Typ: **REFIID**

Ein Verweis auf die GUID (Globally Unique Identifier) der Schnittstelle, die in *ppvFactory* zurückgegeben werden soll. Es wird erwartet, dass dies der Schnittstellenbezeichner (IID) von [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md)ist.

### <a name="ppvfactory-out"></a>ppvFactory [out]

Typ: **\* \* void**

Die Adresse eines Zeigers auf eine Schnittstelle mit der im *riid-Parameter* angegebenen IID. Nach erfolgreicher Rückgabe enthält *\* ppvFactory* (die dereferenzierte Adresse) einen Zeiger auf die erstellte DXCore-Factory.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](../../com/structure-of-com-error-codes.md) [](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|E_NOINTERFACE|Für *riid* wurde ein ungültiger Wert bereitgestellt.|
|E_POINTER|`nullptr` wurde für *ppvFactory* bereitgestellt.|

## <a name="remarks"></a>Hinweise

Für den Zeitraum, in dem ein Verweis auf eine [IDXCoreAdapterFactory-Schnittstelle,](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) eine [IDXCoreAdapterList-Schnittstelle](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) oder eine [IDXCoreAdapter-Schnittstelle](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) vorhanden ist, geben zusätzliche Aufrufe von **DXCoreCreateAdapterFactory,** [IDXCoreAdapterList::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)oder [IDXCoreAdapter::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) Zeiger auf dasselbe Objekt zurück, wodurch die Verweisanzahl der **IDXCoreAdapterFactory-Schnittstelle** erhöht wird.

## <a name="see-also"></a>Siehe auch

[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)