---
description: Die getnextvtrack-Methode ruft den nächsten virtuellen Titel nach einer angegebenen virtuellen Spur ab.
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: 'Iamtimelinecomp:: getnextvtrack-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e5a4500c2b53703a13b509f112453e65c954f96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359758"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a>Iamtimelinecomp:: getnextvtrack-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetNextVTrack` Methode ruft den nächsten virtuellen Titel nach einer angegebenen virtuellen Spur ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvirtualtrack* 
</dt> <dd>

Zeiger auf den vorherigen virtuellen Titel oder **null** , um den ersten virtuellen Titel in der Komposition abzurufen.

</dd> <dt>

*ppnextvirtualtrack* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle der nächsten virtuellen Spur in der Reihenfolge ihrer Priorität.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt s \_ OK zurück, wenn die Methode einen virtuellen Track abruft, \_ andernfalls false.

## <a name="remarks"></a>Bemerkungen

Wenn die Methode erfolgreich ausgeführt wird, weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

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

[**Iamtimelinecomp-Schnittstelle**](iamtimelinecomp.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




