---
description: 'Die GetMediaLength2-Methode ruft die Medien Länge dieses Quell Objekts ab. Diese Methode entspricht iamtimelinesrc:: getmedialength, erfordert jedoch reftime-Werte.'
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: 'Iamtimelinesrc:: GetMediaLength2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: caee510db9ddeda1923327176a634a9011601e4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357319"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a>Iamtimelinesrc:: GetMediaLength2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetMediaLength2` Methode ruft die Medien Länge dieses Quell Objekts ab. Diese Methode entspricht [**iamtimelinesrc:: getmedialength**](iamtimelinesrc-getmedialength.md), erfordert jedoch [**reftime**](reftime.md) -Werte.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMediaLength2(
   REFTIME *pLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pLength* 
</dt> <dd>

Empfängt die Medien Länge in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                     | Beschreibung                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Erfolg.<br/>                                |
| <dl> <dt>**E \_ notbestimmt**</dt> </dl> | Für dieses Objekt sind keine Medien Zeiten festgelegt.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>       | **Null** -Zeigerargument.<br/>              |



 

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

 

 




