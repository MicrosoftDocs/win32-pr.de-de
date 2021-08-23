---
title: IWMDRMEncryptScatter InitEncryptScatter-Methode (Wmdrmsdk.h)
description: Die InitEncryptScatter-Methode initialisiert die IWMDRMEncryptScatter-Schnittstelle zur Verwendung.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- InitEncryptScatter-Methode windows Media Format
- InitEncryptScatter-Methode windows Media Format , IWMDRMEncryptScatter-Schnittstelle
- IWMDRMEncryptScatter-Schnittstelle windows Media Format , InitEncryptScatter-Methode
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
ms.openlocfilehash: 8e83cce80b218d4cc8482d013537b7fae562312f242bc3549f4fa5069b1c677c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027757"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a>IWMDRMEncryptScatter::InitEncryptScatter-Methode

Die **InitEncryptScatter-Methode** initialisiert die **IWMDRMEncryptScatter-Schnittstelle** zur Verwendung.

## <a name="syntax"></a>Syntax


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cStreams* \[ In\]
</dt> <dd>

Anzahl der Elemente im *rgInfos-Array.* Dies ist auch die Anzahl der Streams, die in den zu verschlüsselnden Daten enthalten sind.

</dd> <dt>

*rgInfos* \[ In\]
</dt> <dd>

Array einer oder mehrerer [**WMDRM \_ ENCRYPT \_ SCATTER \_ INFO-Strukturen.**](wmdrm-encrypt-scatter-info.md) Jedes Element enthält Verschlüsselungsinformationen für einen Stream. Die Anzahl der Elemente in diesem Array muss gleich dem Wert von *cStreams* sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[**IWMDRMEncryptScatter-Schnittstelle**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





