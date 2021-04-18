---
title: Iwmdrmentschlüsseln-Entschlüsselungsmethode (wmdrmsdk. h)
description: Die Entschlüsselungsmethode entschlüsselt einen Datenpuffer an Ort und Stelle.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Entschlüsselungsmethode Windows Media-Format
- Entschlüsselungsmethode Windows Media-Format, iwmdrmentschlüsselungsschnittstelle
- Iwmdrmentschlüsselungsschnittstelle Windows Media-Format, Entschlüsselungsmethode
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3c1437bc4b4d2f442c61e54f238f176adf66b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365894"
---
# <a name="iwmdrmdecryptdecrypt-method"></a>Iwmdrmentschlüsselungsmethode::D ecrypt-Methode

Die **Entschlüsselungsmethode** entschlüsselt einen Datenpuffer an Ort und Stelle.

## <a name="syntax"></a>Syntax


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbData* \[ in, out\]
</dt> <dd>

Die zu entschlüsselnden Daten. Wenn die Methode erfolgreich ausgeführt wird, werden diese Daten bei Rückgabe entschlüsselt.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Größe der Daten in Bytes.

</dd> <dt>

*pwmcryptodata* \[ in\]
</dt> <dd>

Zeiger auf eine [**wmdrmcryptodata**](wmdrmcryptodata.md) -Struktur mit zusätzlichen Parametern. Kann **null** sein, wenn der Inhalt mit den Standardparametern verschlüsselt wurde.

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

[**Iwmdrmentschlüsseln-Schnittstelle**](iwmdrmdecrypt.md)
</dt> <dt>

[**Wmdrmcryptodata**](wmdrmcryptodata.md)
</dt> </dl>

 

 





