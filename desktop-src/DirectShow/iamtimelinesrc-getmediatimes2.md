---
description: 'Die GetMediaTimes2-Methode ruft die Start-und Endzeit des Mediums ab. Diese Methode entspricht iamtimelinesrc:: getmediatimes, erfordert jedoch reftime-Werte.'
ms.assetid: c3961c2c-7198-44bd-8734-7301a7c5b21e
title: 'Iamtimelinesrc:: GetMediaTimes2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 779876e542ab51914725b326a0e3b217b893f254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362008"
---
# <a name="iamtimelinesrcgetmediatimes2-method"></a>Iamtimelinesrc:: GetMediaTimes2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `GetMediaTimes2` -Methode ruft die Start-und Endzeit des Mediums ab. Diese Methode entspricht [**iamtimelinesrc:: getmediatimes**](iamtimelinesrc-getmediatimes.md), erfordert jedoch [**reftime**](reftime.md) -Werte.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PStart* 
</dt> <dd>

Empfängt die Start Zeit des Mediums in Sekunden.

</dd> <dt>

*pstopps* 
</dt> <dd>

Empfängt die Endzeit des Mediums in Sekunden.

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

[**Iamtimelinesrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




