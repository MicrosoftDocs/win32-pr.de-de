---
description: Benachrichtigt ein-Objekt, dass es seinen Generator für die angegebene Eigenschaft anzeigen soll.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: 'Iprovidepropertybuilder:: executebuilder-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358255"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a>Iprovidepropertybuilder:: executebuilder-Methode

Benachrichtigt ein-Objekt, dass es seinen Generator für die angegebene Eigenschaft anzeigen soll.

## <a name="syntax"></a>Syntax


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DISPID* \[ in\]
</dt> <dd>

Die DispID der Eigenschaft, für die der Generator angezeigt wird.

</dd> <dt>

*bstringuidbldr* \[ in\]
</dt> <dd>

Der **BSTR** der aufzurufenden Generator-GUID. Dies wird von [**maptopropertybuilder**](iprovidepropertybuilder-mappropertytobuilder.md)zurückgegeben.

</dd> <dt>

*pdispapp* \[ in\]
</dt> <dd>

Auf **null** festgelegt.

</dd> <dt>

*hwndbldrowner* \[ in\]
</dt> <dd>

Ein Handle des übergeordneten Popup-Generator-Fensters.

</dd> <dt>

*pvarvalue* \[ in, out\]
</dt> <dd>

Der aktuelle Wert der Eigenschaft. Dieser Wert kann durch das-Objekt geändert werden und ändert sich in den neuen Wert, wenn *pbactioncommit* den Wert " **true**" hat.

</dd> <dt>

*pbactioncommit* \[ Out, retval\]
</dt> <dd>

Ein Wert, der angibt, ob der Generator eine Aktion für das Objekt ausgeführt hat. Kann verwendet werden, wenn ein Benutzer etwas ändert, und dann im Popup-Generator-Dialogfeld auf OK.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iprovidäpropertybuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




