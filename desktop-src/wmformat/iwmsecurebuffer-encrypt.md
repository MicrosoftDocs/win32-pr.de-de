---
title: Iwmsecurebuffer-Verschlüsselungsmethode (wmdrmsdk. h)
description: Die Methode "verschlüsseln" verschlüsselt einen Datenzeiger.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Verschlüsselungsmethode (Windows Media-Format)
- Verschlüsselungsmethode Windows Media-Format, iwmsecurebuffer-Schnittstelle
- Iwmsecurebuffer-Schnittstelle Windows Media-Format, Methode verschlüsseln
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
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371566"
---
# <a name="iwmsecurebufferencrypt-method"></a>Iwmsecurebuffer:: Verschlüsseln-Methode

Die Methode " **verschlüsseln** " verschlüsselt einen Datenzeiger.

## <a name="syntax"></a>Syntax


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psecurechannel* \[ in\]
</dt> <dd>

Zeiger auf eine sichere Kanal Schnittstelle mit dem Datenzeiger, der verschlüsselt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um Datenzeiger zu verschlüsseln, damit Sie über dll-Grenzen hinweg gesendet werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Entschlüsseln**](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[**Iwmsecurebuffer-Schnittstelle**](iwmsecurebuffer.md)
</dt> </dl>

 

 





