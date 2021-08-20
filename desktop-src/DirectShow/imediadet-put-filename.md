---
description: Die put \_ Filename-Methode gibt den Namen der Quelldatei an, die von der Medienerkennung verwendet werden soll.
ms.assetid: 37bcc7ed-d2c1-4182-b85a-03bad92c5ba7
title: IMediaDet::p ut_Filename-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9a64c0232c77d732bd172bbd46e1a29eef57ae10a96cbaf2a581aeeec5100a20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398266"
---
# <a name="imediadetput_filename-method"></a>IMediaDet::p ut \_ Filename-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `put_Filename` -Methode gibt den Namen der Quelldatei an, die von der Medienerkennung verwendet werden soll.

Rufen Sie diese Methode nicht zweimal für dasselbe MediaDet-Objekt auf. Um diese Schnittstelle mit mehr als einer Quelldatei zu verwenden, erstellen Sie separate Instanzen des MediaDet-Objekts.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Filename(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* \[ In\]
</dt> <dd>

Dateiname der Quelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

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

[**IMediaDet-Schnittstelle**](imediadet.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




