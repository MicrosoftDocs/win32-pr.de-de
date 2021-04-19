---
title: Iwmdrmencryptscatter initencryptscatter-Methode (wmdrmsdk. h)
description: Die initencryptscatter-Methode initialisiert die iwmdrmencryptscatter-Schnittstelle zur Verwendung.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Initencryptscatter-Methode Windows Media-Format
- Initencryptscatter-Methode Windows Media-Format, iwmdrmencryptscatter-Schnittstelle
- Iwmdrmencryptscatter-Schnittstelle Windows Media-Format, initencryptscatter-Methode
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef788ecbe85defc7d3593f0c12c035e516f095eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355896"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a>Iwmdrmencryptscatter:: initencryptscatter-Methode

Die **initencryptscatter** -Methode initialisiert die **iwmdrmencryptscatter** -Schnittstelle zur Verwendung.

## <a name="syntax"></a>Syntax


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cstreams* \[ in\]
</dt> <dd>

Anzahl der Elemente im *rginfos* -Array. Dies ist auch die Anzahl der Streams, die in den zu verschlüsselnden Daten enthalten sind.

</dd> <dt>

*rginfos* \[ in\]
</dt> <dd>

Array von mindestens einer [**WMDRM- \_ Verschlüsselungs \_ Punkt \_ Info**](wmdrm-encrypt-scatter-info.md) -Struktur. Jedes-Element enthält Verschlüsselungs Informationen für einen Datenstrom. Die Anzahl der Elemente in diesem Array muss gleich dem Wert von *cstreams* sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verschlüsselungs Punkt**](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[**Iwmdrmencryptscatter-Schnittstelle**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





