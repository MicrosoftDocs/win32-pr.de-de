---
description: Die GetSubObjectGUIDB-Methode ruft die GUID des Unterobjekts ab, das diesem Zeitachsenobjekt zugeordnet ist. Diese Methode entspricht IAMTimelineObj::GetSubObjectGUID, empfängt jedoch einen BSTR-Wert.
ms.assetid: 693cafda-78c8-4ba4-90d7-23fedcd1fc52
title: IAMTimelineObj::GetSubObjectGUIDB-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79cf7c6a0b3f162f3f3baee2a46cfc0c2c2b61271b19e57549c73b4faa0594bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155381"
---
# <a name="iamtimelineobjgetsubobjectguidb-method"></a>IAMTimelineObj::GetSubObjectGUIDB-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `GetSubObjectGUIDB` -Methode ruft die GUID des Unterobjekts ab, das diesem Zeitachsenobjekt zugeordnet ist. Diese Methode entspricht [**IAMTimelineObj::GetSubObjectGUID,**](iamtimelineobj-getsubobjectguid.md)empfängt jedoch einen **BSTR-Wert.**

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSubObjectGUIDB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Empfängt eine Zeichenfolge, die die Unterobjekt-GUID darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die -Methode ordnet Arbeitsspeicher für die Zeichenfolge zu. Die Anwendung muss **SysFreeString aufrufen,** um den Arbeitsspeicher frei zu machen.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




