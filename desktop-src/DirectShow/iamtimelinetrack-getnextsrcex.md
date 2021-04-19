---
description: Die getnexzrcex-Methode ruft die nächste Quelle nach der angegebenen Quelle ab.
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: 'Iamtimelinetrack:: getnextrcex-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrcEx
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 274a4f6800d995e2b456dbd55adf81cf82aa84a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369434"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a>Iamtimelinetrack:: getnexzrcex-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetNextSrcEx` Methode ruft die nächste Quelle nach der angegebenen Quelle ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextSrcEx(
        IAMTimelineObj *pLast,
  [out] IAMTimelineObj **ppNext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bildet* 
</dt> <dd>

Zeiger auf das vorherige Quell Objekt oder **null** , um die erste Quelle in der Spur abzurufen.

</dd> <dt>

*ppnext* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des nächsten Quell Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "s OK" zurück \_ , wenn die Methode eine Quelle abruft, \_ andernfalls "false".

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

[**Iamtimelinetrack-Schnittstelle**](iamtimelinetrack.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




