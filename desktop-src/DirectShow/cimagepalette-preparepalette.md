---
description: Die PreparePalette-Methode richtet eine Palette basierend auf einem Medientyp des besitzenden Filters ein.
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: Cimagepalette. PreparePalette-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.PreparePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369404"
---
# <a name="cimagepalettepreparepalette-method"></a>Cimagepalette. PreparePalette-Methode

Die- `PreparePalette` Methode richtet eine Palette auf der Grundlage eines Medientyps aus dem besitzenden Filter ein.

## <a name="syntax"></a>Syntax


```C++
HRESULT PreparePalette(
   const CMediaType *pmtNew,
   const CMediaType *pmtOld,
         LPSTR      szDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmtnew* 
</dt> <dd>

Zeiger auf den neuen Medientyp. Der Format Block muss eine [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur sein.

</dd> <dt>

*pmtold* 
</dt> <dd>

Zeiger auf den alten Medientyp. Wenn der Medientyp zum ersten Mal festgelegt wird, kann dieser Parameter ein leerer Typ ohne Format Block sein. Andernfalls muss der Format Block eine **videoinfoheader** -Struktur sein.

</dd> <dt>

*szdevice* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen des Anzeige Geräts enthält, wie von der GDI-Funktion " **EnumDisplayDevices** " zurückgegeben. Legen Sie diesen Parameter auf **null** fest, um das Haupt Anzeigegerät zu verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt s \_ OK zurück, wenn die Palette aktualisiert wurde, oder s \_ false, wenn sich die Palette nicht geändert hat.

## <a name="remarks"></a>Bemerkungen

Wenn die Palette aktualisiert werden muss, führt diese Methode die folgenden Aktionen aus:

-   Ruft [**cimagepalette:: makepalette**](cimagepalette-makepalette.md) auf, um eine neue logische Palette zu erstellen.
-   Sendet ein [**\_ \_ geändertes**](ec-palette-changed.md) Ereignis der EC-Palette an den Filter Diagramm-Manager.
-   Ruft [**cbasewindow:: SetPalette**](cbasewindow-setpalette.md) für das **cbasewindow** -Objekt auf.
-   Ruft [**cdrawimage:: incrementpaletteversion**](cdrawimage-incrementpaletteversion.md) für das **cdrawimage** -Objekt auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagepalette-Klasse**](cimagepalette.md)
</dt> </dl>

 

 




