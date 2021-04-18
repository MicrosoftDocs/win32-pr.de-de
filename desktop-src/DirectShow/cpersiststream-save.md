---
description: Speichert die Filterdaten in dem angegebenen Stream.
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: Cpersiststream. Save-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361294"
---
# <a name="cpersiststreamsave-method"></a>Cpersiststream. Save-Methode

Speichert die Filterdaten in dem angegebenen Stream.

## <a name="syntax"></a>Syntax


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstm* 
</dt> <dd>

Zeiger auf den Stream, in dem Daten gespeichert werden sollen.

</dd> <dt>

*Klartext* 
</dt> <dd>

Flag, das angibt, ob das geänderte Flag des aktuellen Streams zurückgesetzt werden soll. " **True** " gibt zurück (Wenn die Methode als Teil eines Speicher Vorgangs aufgerufen wird, ist der Wert normalerweise **true**; wenn er als Teil eines "Speichern unter"-Vorgangs aufgerufen wird, ist der Wert in der Regel " **false**".)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion implementiert die **IPersistStream:: Save** -Methode. Er ruft den **Schreib** Vorgang mit der Softwareversion auf, ruft [**cpersiststream:: Write**](cpersiststream-writetostream.md) Team Access Stream mit dem Stream in *pstm* auf und setzt die mPS-bereinigen zurück. **\_**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PStream. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpersiststream-Klasse**](cpersiststream.md)
</dt> </dl>

 

 




