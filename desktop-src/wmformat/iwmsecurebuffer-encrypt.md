---
title: IWMSecureBuffer Encrypt-Methode (Wmdrmsdk.h)
description: Die Encrypt-Methode verschlüsselt einen Datenzeiger.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Encrypt method windows Media Format
- Encrypt method windows Media Format , IWMSecureBuffer interface
- IWMSecureBuffer-Schnittstelle windows Media Format , Encrypt-Methode
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e5badce8249e5d6b9d2460fec0e72ef4ca4b81f5b8ffa0d3edd83729f98bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808310"
---
# <a name="iwmsecurebufferencrypt-method"></a>IWMSecureBuffer::Encrypt-Methode

Die **Encrypt-Methode** verschlüsselt einen Datenzeiger.

## <a name="syntax"></a>Syntax


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSecureChannel* \[ In\]
</dt> <dd>

Zeiger auf eine sichere Kanalschnittstelle, die den zu verschlüsselnden Datenzeiger enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, um Datenzeker zu verschlüsseln, damit sie über DLL-Grenzen hinweg gesendet werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Entschlüsseln**](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[**IWMSecureBuffer-Schnittstelle**](iwmsecurebuffer.md)
</dt> </dl>

 

 





