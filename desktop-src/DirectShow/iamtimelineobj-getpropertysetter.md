---
description: Die GetPropertySetter-Methode ruft den Eigenschaftensetter des Objekts ab. Wenn das -Objekt gerendert wird, werden die im Eigenschaftensetter enthaltenen Eigenschafteninformationen auf das -Objekt angewendet.
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: IAMTimelineObj::GetPropertySetter-Methode (Qedit.h)
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
ms.openlocfilehash: fd86d1c0b8334c1587745278ee499e38113887bb074770f49364429f71fa53da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831080"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a>IAMTimelineObj::GetPropertySetter-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetPropertySetter` -Methode ruft den Eigenschaftensetter des Objekts ab. Wenn das -Objekt gerendert wird, werden die im Eigenschaftensetter enthaltenen Eigenschafteninformationen auf das -Objekt angewendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IPropertySetter-Schnittstelle**](ipropertysetter.md) des Eigenschaftensetters. Wenn das Objekt keinen Eigenschaftensetter hat, wird der Wert auf **NULL** festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn der in *pVal* zurückgegebene Wert nicht **NULL** ist, verfügt die **IPropertySetter-Schnittstelle** über einen ausstehenden Verweiszähler. Stellen Sie sicher, dass Sie die Schnittstelle freigeben, wenn Sie sie nicht mehr verwenden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




