---
description: Die setpropertysetter-Methode legt den Eigenschaften Setter des Objekts fest. Wenn das Objekt gerendert wird, werden die im Eigenschaften Setter enthaltenen Eigenschafts Informationen auf das Objekt angewendet. Diese Methode wird bei Übergangs-und Effekt Objekten aufgerufen.
ms.assetid: 3ce2fe50-a884-4da4-95b5-9c97e188f819
title: 'Iamtimelineobj:: setpropertysetter-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cf8cea3abbcc25c91a398af1af61b0ff4de0cd5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371670"
---
# <a name="iamtimelineobjsetpropertysetter-method"></a>Iamtimelineobj:: setpropertysetter-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `SetPropertySetter` -Methode legt den Eigenschaften Setter des Objekts fest. Wenn das Objekt gerendert wird, werden die im Eigenschaften Setter enthaltenen Eigenschafts Informationen auf das Objekt angewendet. Diese Methode wird bei Übergangs-und Effekt Objekten aufgerufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPropertySetter(
   IPropertySetter *newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* 
</dt> <dd>

Ein Zeiger auf die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle des Eigenschaften Setters.

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

[**Iamtimelineobj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




