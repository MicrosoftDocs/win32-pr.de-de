---
description: 'Die getdefaulteffectb-Methode ruft den Standardeffekt ab. Diese Methode entspricht iamtimeline:: getdefaulteffect, empfängt aber einen BSTR-Wert anstelle einer GUID.'
ms.assetid: 62c37a61-9875-4140-8552-83d82c060715
title: 'Iamtimeline:: getdefaulteffectb-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 01b82c42c34e3146bbad5560d516aef55225a3d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365570"
---
# <a name="iamtimelinegetdefaulteffectb-method"></a>Iamtimeline:: getdefaulteffectb-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetDefaultEffectB` Methode ruft den Standardeffekt ab. Diese Methode entspricht [**iamtimeline:: getdefaulteffect**](iamtimeline-getdefaulteffect.md), empfängt aber einen **BSTR** -Wert anstelle einer GUID.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDefaultEffectB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguid* \[ Out, retval\]
</dt> <dd>

Empfängt einen **BSTR** -Wert, der die GUID des Standard Effekts darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die-Methode ordnet Speicher für die Zeichenfolge zu. Die Anwendung muss **SysFreeString** aufzurufen, um den Arbeitsspeicher freizugeben.

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

[**Iamtimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




