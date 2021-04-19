---
description: Die gezmartrecompressformat-Methode ruft das aktuelle Komprimierungs Format für die intelligente Neukomprimierung ab.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: 'Iamtimelinegroup:: gezmartrecompressformat-Methode (qedit. h)'
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
ms.openlocfilehash: 8560bb9d8da6904cf74b62ffd238b234e9c74ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358108"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a>Iamtimelinegroup:: gezmartrecompressformat-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetSmartRecompressFormat` Methode ruft das aktuelle Komprimierungs Format für die intelligente Neukomprimierung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppformat* 
</dt> <dd>

Empfängt einen Zeiger auf eine [**SCompFmt0**](scompfmt0.md) -Struktur, die als Zeiger auf einen Long-Typ umgewandelt wird. Wenn die Methode fehlschlägt, wird der Wert auf **null** festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn die Anwendung kein intelligentes Komprimierungs Format festgelegt hat (durch Aufrufen von [**iamtimelinegroup:: setionmartrecompressformat**](iamtimelinegroup-setsmartrecompressformat.md)), ist das von dieser Methode zurückgegebene Format ungültig. Rufen Sie die [**iamtimelinegroup:: issmartrecompressformatset**](iamtimelinegroup-issmartrecompressformatset.md) -Methode auf, um zu bestimmen, ob ein Komprimierungs Format festgelegt wurde.

Wenn die Methode erfolgreich ausgeführt wird, muss der Aufrufer den zurückgegebenen Medientyp freigeben und die [**SCompFmt0**](scompfmt0.md) -Struktur löschen:


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



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

 

 




