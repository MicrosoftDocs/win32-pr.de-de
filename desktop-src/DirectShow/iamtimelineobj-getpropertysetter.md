---
description: Die getpropertysetter-Methode ruft den Eigenschaften Setter des Objekts ab. Wenn das Objekt gerendert wird, werden die im Eigenschaften Setter enthaltenen Eigenschafts Informationen auf das Objekt angewendet.
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: 'Iamtimelineobj:: getpropertysetter-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4410a0b63a0228d9e8e403ef1f0403d1968ad639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373923"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a>Iamtimelineobj:: getpropertysetter-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `GetPropertySetter` -Methode ruft den Eigenschaften Setter des Objekts ab. Wenn das Objekt gerendert wird, werden die im Eigenschaften Setter enthaltenen Eigenschafts Informationen auf das Objekt angewendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PVal* \[ Out, retval\]
</dt> <dd>

Empfängt einen Zeiger auf die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle des Eigenschaften Setters. Wenn das Objekt keinen Eigenschaften Setter aufweist, wird der Wert auf **null** festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn der in *PVal* zurückgegebene Wert nicht **null** ist, weist die **ipropertysetter** -Schnittstelle einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

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

[**Iamtimelineobj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




