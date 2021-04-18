---
title: Iwmsecurebuffer-Entschlüsselungsmethode (wmdrmsdk. h)
description: Die Entschlüsselungsmethode entschlüsselt einen Datenzeiger, der durch Aufrufen der Verschlüsselungsmethode verschlüsselt wurde.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Entschlüsselungsmethode Windows Media-Format
- Entschlüsselungsmethode Windows Media-Format, iwmsecurebuffer-Schnittstelle
- Iwmsecurebuffer-Schnittstelle Windows Media-Format, Entschlüsselungsmethode
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
ms.openlocfilehash: a6f48ae389090840e085c90b0bc5444e7cd6784e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371366"
---
# <a name="iwmsecurebufferdecrypt-method"></a>Iwmsecurebuffer::D ecrypt-Methode

Die **Entschlüsselungsmethode** entschlüsselt einen Datenzeiger, der durch Aufrufen der [**Verschlüsselungs**](iwmsecurebuffer-encrypt.md) Methode verschlüsselt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psecurechannel* \[ in\]
</dt> <dd>

Zeiger auf eine sichere Kanal Schnittstelle, die den verschlüsselten Datenzeiger enthält.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verschlüsseln**](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[**Iwmsecurebuffer-Schnittstelle**](iwmsecurebuffer.md)
</dt> </dl>

 

 





