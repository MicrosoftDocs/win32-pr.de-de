---
title: IWMSecureBuffer Decrypt-Methode (Wmdrmsdk.h)
description: Die Decrypt-Methode entschlüsselt einen Datenzeiger, der durch Aufrufen der Encrypt-Methode verschlüsselt wurde.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Decrypt method windows Media Format
- Decrypt method windows Media Format , IWMSecureBuffer interface
- IWMSecureBuffer-Schnittstelle windows Media Format , Decrypt-Methode
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Decrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9867cb6476ab0a2838903c906f662032e14dfb0d4fa0547b045672e03b6ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930100"
---
# <a name="iwmsecurebufferdecrypt-method"></a>IWMSecureBuffer::D ecrypt-Methode

Die **Decrypt-Methode** entschlüsselt einen Datenzeiger, der durch Aufrufen der [**Encrypt-Methode verschlüsselt**](iwmsecurebuffer-encrypt.md) wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSecureChannel* \[ In\]
</dt> <dd>

Zeiger auf eine sichere Kanalschnittstelle, die den verschlüsselten Datenzeiger enthält.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Encrypt**](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[**IWMSecureBuffer-Schnittstelle**](iwmsecurebuffer.md)
</dt> </dl>

 

 





