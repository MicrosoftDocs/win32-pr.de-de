---
description: Die setmedialength-Methode gibt die Dauer der Quelldatei an.
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: 'Iamtimelinesrc:: setmedialength-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d585e9076606a77c8ecd03701ad41ab421eacd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369258"
---
# <a name="iamtimelinesrcsetmedialength-method"></a>Iamtimelinesrc:: setmedialength-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetMediaLength` Methode gibt die Dauer der Quelldatei an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Länge* 
</dt> <dd>

Medien Länge in 100-Nanosecond-Einheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Sie können potenzielle Renderingfehler vermeiden, indem Sie die Medien Länge festlegen, bevor Sie die Zeit für das Medien Ende festlegen. Wenn Sie die Zeit für das Beenden des Mediums festlegen, wird der von des auf die Medien Länge überprüft.

Diese Methode überprüft den *length* -Parameter nicht, aber der Wert muss der tatsächlichen Dauer der Quelldatei entsprechen. Rufen Sie die Dauer der Quelldatei ab, indem [**Sie imediadet:: get \_ streamlength**](imediadet-get-streamlength.md)aufrufen.

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

 

 




