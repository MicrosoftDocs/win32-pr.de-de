---
description: 'Die Methode "frei-Eigenschaften" gibt Ressourcen frei, die von der ipropertysetter:: getrequiemethode zugeordnet werden. Rufen Sie diese Methode nach dem Aufrufen von gettial auf, und übergeben Sie dabei die von gettial zurückgegebenen Strukturen.'
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'Ipropertysetter:: frerequiproperemethode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3cc90d094d3213b5b68f61585296bcb21ebbf5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352875"
---
# <a name="ipropertysetterfreeprops-method"></a>Ipropertysetter:: frerequismethode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die-Methode gibt Ressourcen frei, `FreeProps` die von der [**ipropertysetter:: getrequiemethode**](ipropertysetter-getprops.md) zugeordnet werden. Rufen Sie diese Methode nach dem Aufrufen von **gettial** auf, und übergeben Sie dabei die von **gettial** zurückgegebenen Strukturen.

## <a name="syntax"></a>Syntax


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cparameams* \[ in\]
</dt> <dd>

Die Anzahl der Elemente *im Array Array* .

</dd> <dt>

mit einem *paar* \[ in\]
</dt> <dd>

Zeiger auf ein Array von [**Dexter- \_ param**](dexter-param.md) -Strukturen.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Zeiger auf ein Array von [**Dexter- \_ Wert**](dexter-value.md) Strukturen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

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

 

 




