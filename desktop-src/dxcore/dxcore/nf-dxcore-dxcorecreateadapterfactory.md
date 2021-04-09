---
title: DXCoreCreateAdapterFactory
description: Erstellt eine DXCore-AdapterFactory, die Sie verwenden können, um weitere DXCore-Objekte zu generieren.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3f5164578da87af8f4d92c3bedcecb6f3dbaa95e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948994"
---
# <a name="dxcorecreateadapterfactory-function"></a>Dxcorecreateadapterfactory-Funktion

## <a name="description"></a>BESCHREIBUNG

Erstellt eine DXCore-AdapterFactory, die Sie verwenden können, um weitere DXCore-Objekte zu generieren. Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).

## <a name="parameters"></a>Parameter

### <a name="riid"></a>riid

Typ: **refID**

Ein Verweis auf die Globally Unique Identifier (GUID) der Schnittstelle, die in *ppvfactory* zurückgegeben werden soll. Dies wird als Schnittstellen Bezeichner (IID) von [idxcoreadapterfactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md)erwartet.

### <a name="ppvfactory-out"></a>ppvfactory [out]

Typ: **void \* \***

Die Adresse eines Zeigers auf eine Schnittstelle mit der im *riid* -Parameter angegebenen IID. Bei erfolgreicher Rückgabe enthält *\* ppvfactory* (die Dereferenzierte Adresse) einen Zeiger auf die erstellte DXCore-Factory.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|E_NOINTERFACE|Für *riid* wurde ein ungültiger Wert angegeben.|
|E_POINTER|`nullptr` wurde für *ppvfactory* bereitgestellt.|

## <a name="remarks"></a>Bemerkungen

Für den Zeitraum, in dem ein Verweis auf einer [idxcoreadapterfactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) -Schnittstelle vorhanden ist, eine [idxcoreadapterlist](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) -Schnittstelle oder eine [idxcoreadapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) -Schnittstelle, zusätzliche Aufrufe von **dxcorecreateadapterfactory**, [idxcoreadapterlist:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)oder [idxcoreadapter:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) geben Zeiger auf dasselbe Objekt zurück und erhöhen den Verweis Zähler der **idxcoreadapterfactory** -Schnittstelle.

## <a name="see-also"></a>Siehe auch

[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)