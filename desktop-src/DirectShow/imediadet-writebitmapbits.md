---
description: Die WriteBitmapBits-Methode ruft einen Videoframe zur angegebenen Medienzeit ab und schreibt ihn in eine Datei. Der Videoframe hat immer das 24-Bit-RGB-Format.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: IMediaDet::WriteBitmapBits-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc2a967f5b0e99c50317e9dc226a4b345c6790a8ce2b6e5d42eb50dfdc3b105b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154155"
---
# <a name="imediadetwritebitmapbits-method"></a>IMediaDet::WriteBitmapBits-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `WriteBitmapBits` -Methode ruft einen Videoframe zur angegebenen Medienzeit ab und schreibt ihn in eine Datei. Der Videoframe hat immer das 24-Bit-RGB-Format.

## <a name="syntax"></a>Syntax


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StreamTime* 
</dt> <dd>

Zeitpunkt, zu dem der Videoframe abgerufen werden soll.

</dd> <dt>

*Width* 
</dt> <dd>

Breite des Bilds in Pixel.

</dd> <dt>

*Height* 
</dt> <dd>

Höhe des Bilds in Pixel.

</dd> <dt>

*Filename* 
</dt> <dd>

Pfad der Datei, in der die Bitmap gespeichert werden soll. Wenn die Datei bereits vorhanden ist, wird sie von dieser Methode überschrieben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "S \_ OK it successful" zurück. Andernfalls gibt einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt. Mögliche Fehlercodes:



| Rückgabecode                                                                                             | Beschreibung                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>           | Der Filter [**Sample Grabber konnte dem**](sample-grabber-filter.md) Diagramm nicht hinzugefügt werden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                  | Fehler.<br/>                                                                               |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Nicht genügend Arbeitsspeicher.<br/>                                                                   |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>            | Unerwarteter Fehler.<br/>                                                                      |
| <dl> <dt>**STG \_ E \_ ACCESSDENIED**</dt> </dl>     | Datei kann nicht überschrieben werden.<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Ungültiger Medientyp.<br/>                                                                    |



 

## <a name="remarks"></a>Hinweise

Legen Sie vor dem Aufrufen dieser Methode den Dateinamen und stream fest, indem Sie [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) und [**IMediaDet::p ut \_ CurrentStream aufrufen.**](imediadet-put-currentstream.md)

Diese Methode versetzt die Medienerkennung in den Bitmap-Greifmodus. Sobald diese Methode aufgerufen wurde, funktionieren die verschiedenen Streaminformationsmethoden in **IMediaDet** nicht mehr, es sei denn, Sie erstellen eine neue Instanz der Medienerkennung.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMediaDet-Schnittstelle**](imediadet.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




