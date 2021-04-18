---
description: Die GetEffect-Methode ruft den Effekt auf der angegebenen Prioritäts Ebene ab.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: 'Iamtimelineeffectable:: GetEffect-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7a769fca28ea1f8f698b23de7df6b7c15f05234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365841"
---
# <a name="iamtimelineeffectablegeteffect-method"></a>Iamtimelineeffectable:: GetEffect-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die **GetEffect** -Methode ruft den Effekt auf der angegebenen Prioritäts Ebene ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppfx* \[ vorgenommen\]
</dt> <dd>

Empfängt die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Effekts.

</dd> <dt>

*,* 
</dt> <dd>

Prioritätsstufe des abzurufenden Effekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen HRESULT-Wert zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                               | Beschreibung                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Keine Auswirkung mit der angegebenen Priorität,<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>                             |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeigerargument.<br/>           |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Methode S OK zurückgibt \_ , weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

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

[**Iamtimelineeffectable-Schnittstelle**](iamtimelineeffectable.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




