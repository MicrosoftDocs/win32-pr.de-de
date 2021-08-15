---
description: Die FreeProps-Methode gibt von der IPropertySetter::GetProps-Methode zugeordnete Ressourcen frei. Rufen Sie diese Methode nach dem Aufruf von GetProps auf, und übergeben Sie ihr die von GetProps zurückgegebenen Strukturen.
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: IPropertySetter::FreeProps-Methode (Qedit.h)
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
ms.openlocfilehash: 34529c7d78ad36a87eb441f624af8daf1167a77148758ff376feacc70250f18e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397551"
---
# <a name="ipropertysetterfreeprops-method"></a>IPropertySetter::FreeProps-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `FreeProps` -Methode gibt von der [**IPropertySetter::GetProps-Methode zugeordnete Ressourcen**](ipropertysetter-getprops.md) frei. Rufen Sie diese Methode nach dem Aufruf **von GetProps auf,** und übergeben Sie ihr die von **GetProps zurückgegebenen Strukturen.**

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

*cParams* \[ In\]
</dt> <dd>

Die Anzahl der Elemente im *paParam-Array.*

</dd> <dt>

*paParam* \[ In\]
</dt> <dd>

Zeiger auf ein Array von [**DEXTER \_ PARAM-Strukturen.**](dexter-param.md)

</dd> <dt>

*paValue* \[ In\]
</dt> <dd>

Zeiger auf ein Array von [**DEXTER \_ VALUE-Strukturen.**](dexter-value.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPropertySetter-Schnittstelle**](ipropertysetter.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




