---
description: Die GetSmartRecompressFormat-Methode ruft das aktuelle Komprimierungsformat für die intelligente Rekomprimierung ab.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: IAMTimelineGroup::GetSmartRecompressFormat-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8d568bdf0446533df9391c1c0b30382b9a56ecdf0ed788d64c48c38ddf0684a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400728"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a>IAMTimelineGroup::GetSmartRecompressFormat-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `GetSmartRecompressFormat` -Methode ruft das aktuelle Komprimierungsformat für die intelligente Rekomprimierung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppFormat* 
</dt> <dd>

Empfängt einen Zeiger auf eine [**SCompFmt0-Struktur,**](scompfmt0.md) die als Zeiger auf eine long-Struktur umgerüstt wird. Wenn bei der Methode ein Fehler auftritt, wird der Wert auf **NULL festgelegt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn die Anwendung kein intelligentes Komprimierungsformat festgelegt hat (durch Aufrufen von [**IAMTimelineGroup::SetSmartRecompressFormat),**](iamtimelinegroup-setsmartrecompressformat.md)ist das von dieser Methode zurückgegebene Format ungültig. Rufen Sie [**die IAMTimelineGroup::IsSmartRecompressFormatSet-Methode**](iamtimelinegroup-issmartrecompressformatset.md) auf, um zu bestimmen, ob ein Komprimierungsformat festgelegt wurde.

Wenn die Methode erfolgreich ist, muss der Aufrufer den zurückgegebenen Medientyp frei geben und die [**SCompFmt0-Struktur**](scompfmt0.md) löschen:


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimelineGroup-Schnittstelle**](iamtimelinegroup.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




