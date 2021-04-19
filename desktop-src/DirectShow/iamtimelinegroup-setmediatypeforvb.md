---
description: Die setmediatypeer forvb-Methode gibt den Gruppen Medientyp für Automatisierungs Clients an.
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: 'Iamtimelinegroup:: setmediatypeer forvb-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1371b1d6c906666ca30e5df2d26dbe20eddf1745
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370283"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a>Iamtimelinegroup:: setmediatypeer forvb-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetMediaTypeForVB` Methode gibt den Gruppen Medientyp für Automation-Clients an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Val* \[ in\]
</dt> <dd>

Der-Wert, der den Medientyp angibt. Legen Sie den Wert für Video auf 0 oder für Audiodaten den Wert 1 fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist für Automatisierungs Clients vorgesehen. Verwenden Sie für C++-Anwendungen die [**iamtimelinegroup:: setmediatype**](iamtimelinegroup-setmediatype.md) -Methode.

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

[**Iamtimelinegroup-Schnittstelle**](iamtimelinegroup.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




