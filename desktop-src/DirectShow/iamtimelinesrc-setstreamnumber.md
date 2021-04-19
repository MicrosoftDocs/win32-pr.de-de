---
description: Die setstreamnumber-Methode gibt an, welcher Stream aus der mit diesem Quell Objekt verknüpften Quelldatei gelesen werden soll.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'Iamtimelinesrc:: setstreamnumber-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32deec91d4ae0fe55b4574344dd357932856db81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373857"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a>Iamtimelinesrc:: setstreamnumber-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetStreamNumber` Methode gibt den Stream an, der aus der diesem Quell Objekt zugeordneten Quelldatei gelesen werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Val* 
</dt> <dd>

Die streamnummer aus dem Satz von Streams, der mit dem Medientyp der übergeordneten Gruppe übereinstimmt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Der *Val* -Parameter gibt eine streamnummer aus dem Satz von Streams an, der mit dem Medientyp der übergeordneten Gruppe übereinstimmt, nicht aus dem gesamten Satz von Datenströmen in der Quelldatei. Angenommen, eine Datei enthält z. b. zwei Videostreams und zwei Audiodatenströme. Wenn sich das Quell Objekt innerhalb einer Videogruppe befindet, wählt das Festlegen von *Val* auf 0 den ersten Videostream aus. Der Aufrufer ist für das Angeben einer gültigen streamnummer verantwortlich.

Die streamnummer ist standardmäßig 0 (null).

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

 

 




