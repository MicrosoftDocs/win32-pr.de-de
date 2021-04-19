---
description: Die getcutsonly-Methode bestimmt, ob der Übergang als Ausschneiden gerendert wird. Wenn dies der Fall ist, tritt der Übergang sofort am Ausschneide Punkt auf.
ms.assetid: d7959816-1152-4bc4-b3f8-bed69b450530
title: 'Iamtimelinetrans:: getcutsonly-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d3bbec55ddfe77c053135054fde9b64efce516a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367189"
---
# <a name="iamtimelinetransgetcutsonly-method"></a>Iamtimelinetrans:: getcutsonly-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetCutsOnly` Methode bestimmt, ob der Übergang als Ausschneiden gerendert wird. Wenn dies der Fall ist, tritt der Übergang sofort am Ausschneide Punkt auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCutsOnly(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* 
</dt> <dd>

Empfängt einen booleschen Wert, der angibt, ob der Übergang als Ausschneiden gerendert wird. **True** gibt an, dass der Übergang eine sofortige Ausschneide ist. Wenn der Wert **false** ist, tritt der Übergang über die normale Dauer auf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

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

[**Iamtimelinetrans-Schnittstelle**](iamtimelinetrans.md)
</dt> <dt>

[**Iamtimelinetrans:: setcutsonly**](iamtimelinetrans-setcutsonly.md)
</dt> <dt>

[**Iamtimelinetrans:: getcutpoint**](iamtimelinetrans-getcutpoint.md)
</dt> <dt>

[**Iamtimeline:: transitionsenabled**](iamtimeline-transitionsenabled.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




