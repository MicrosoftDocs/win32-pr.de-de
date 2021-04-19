---
description: Die makeidentitypalette-Methode versucht, eine &\# 0034;-Identitäts Palette zu erstellen &\# 0034; definiert als eine, die direkt der im Anzeigegerät ausgewählten Palette zugeordnet ist.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: Cimagepalette. makeidentitypalette-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e105652108e74907375408f0bd8946c69194202
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370532"
---
# <a name="cimagepalettemakeidentitypalette-method"></a>Cimagepalette. makeidentitypalette-Methode

Die `MakeIdentityPalette` Methode versucht, eine "Identitäts Palette" als eine zu definieren, die direkt der im Anzeigegerät ausgewählten Palette zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pentry* 
</dt> <dd>

Zeiger auf ein Array von paletteneinträgen.

</dd> <dt>

*icolours* 
</dt> <dd>

Anzahl der Paletteneinträge in *Pentry*.

</dd> <dt>

*szdevice* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen des Anzeige Geräts enthält, wie von der GDI-Funktion " **EnumDisplayDevices** " zurückgegeben. Legen Sie diesen Parameter auf **null** fest, um das Haupt Anzeigegerät zu verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg s OK oder \_ false zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode vergleicht die reservierten Einträge in der Systempalette mit den entsprechenden Einträgen im *Pentry* -Array. Wenn Sie genau übereinstimmen, legt die-Methode das PC- \_ nocollapse-Flag in den restlichen (nicht reservierten) paletteneinträgen in *Pentry* fest. Mit diesem Flag wird verhindert, dass der GDI logische Paletteneinträge zu System paletteneinträgen zuordnet.

Die [**cimagepalette:: makepalette**](cimagepalette-makepalette.md) -Methode ruft diese Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cimagepalette-Klasse**](cimagepalette.md)
</dt> </dl>

 

 




