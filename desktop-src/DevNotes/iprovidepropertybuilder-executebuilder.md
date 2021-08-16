---
description: Benachrichtigt ein Objekt, dass es seinen Generator für die angegebene Eigenschaft anzeigen soll.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: IProvidePropertyBuilder::ExecuteBuilder-Methode
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
ms.openlocfilehash: 9aef31629cac755d5689de929c02fbc8d9b816bf868a48bd59df3d08c911d9b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827245"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a>IProvidePropertyBuilder::ExecuteBuilder-Methode

Benachrichtigt ein Objekt, dass es seinen Generator für die angegebene Eigenschaft anzeigen soll.

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

*dispid* \[ In\]
</dt> <dd>

Die DISPID der Eigenschaft, für die der Generator angezeigt wird.

</dd> <dt>

*bstrGuidBldr* \[ In\]
</dt> <dd>

Der **BSTR der** aufrufenden Generator-GUID. Dies wird von [**MapToPropertyBuilder zurückgegeben.**](iprovidepropertybuilder-mappropertytobuilder.md)

</dd> <dt>

*pdispApp* \[ In\]
</dt> <dd>

Legen Sie auf **NULL fest.**

</dd> <dt>

*hwndBldrOwner* \[ In\]
</dt> <dd>

Ein Handle für das übergeordnete Popup-Generatorfenster.

</dd> <dt>

*pvarValue* \[ in, out\]
</dt> <dd>

Der aktuelle Wert der Eigenschaft. Dieser Wert kann vom -Objekt geändert werden und ändert sich in den neuen Wert, *wenn pbActionCommitted* **TRUE ist.**

</dd> <dt>

*pbActionCommitted* \[ out, retval\]
</dt> <dd>

Ein -Wert, der angibt, ob der Generator eine Aktion für das -Objekt ausgeführt hat. Kann verwendet werden, wenn ein Benutzer etwas ändert, und dann im Popup-Generatordialogfeld auf OK drückt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IProvidePropertyBuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




