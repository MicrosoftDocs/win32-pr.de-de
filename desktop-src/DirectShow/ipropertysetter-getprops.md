---
description: Die GetProperties-Methode ruft die Eigenschaften, die für dieses Objekt festgelegt sind, mit den entsprechenden Werten ab.
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: 'Ipropertysetter:: getrequiemethode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f512ce672cbbaca6556ad644f21c684130eb28e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365955"
---
# <a name="ipropertysettergetprops-method"></a>Ipropertysetter:: getrequismethode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetProps` Methode ruft die für dieses-Objekt festgelegten Eigenschaften mit ihren entsprechenden Werten ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcparametriams* \[ vorgenommen\]
</dt> <dd>

Empfängt die Anzahl der in einem *paar* zurückgegebenen Strukturen.

</dd> <dt>

mit einem *paar* \[ vorgenommen\]
</dt> <dd>

Adresse eines Zeigers auf ein Array von [**Dexter \_ param**](dexter-param.md) -Strukturen.

</dd> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Adresse eines Zeigers auf ein Array von [**Dexter- \_ Wert**](dexter-value.md) Strukturen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Der **nvalues** -Member gibt für jede Eigenschaft, die in der-Eigenschaft zurückgegeben wird, die Anzahl der der Eigenschaft zugeordneten [**Dexter- \_ Wert**](dexter-value.md) *Strukturen an.* Die Paare werden für jede Eigenschaft in aufsteigender Reihenfolge zurückgegeben.

Wenn Sie mit der Verwendung der zurückgegebenen Strukturen fertig sind, müssen Sie [**ipropertysetter:: Free-Eigenschaften**](ipropertysetter-freeprops.md) aufrufen, um die von dieser Methode zugeordneten Ressourcen freizugeben.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie alle Werte in einer Instanz des Eigenschaften Setter durchlaufen werden:


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ipropertysetter-Schnittstelle**](ipropertysetter.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




