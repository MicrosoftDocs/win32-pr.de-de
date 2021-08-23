---
title: IWMDRMDecrypt Decrypt-Methode (Wmdrmsdk.h)
description: Die Decrypt-Methode entschlüsselt einen Datenpuffer an Ort und Stelle.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Decrypt method windows Media Format
- Decrypt method windows Media Format , IWMDRMDecrypt interface
- IWMDRMDecrypt interface windows Media Format , Decrypt method
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
ms.openlocfilehash: 7be82ec976da39103698b93a09b3d5235c8c8ee712783ca8284dc7b18c6a8a27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027747"
---
# <a name="iwmdrmdecryptdecrypt-method"></a>IWMDRMDecrypt::D ecrypt-Methode

Die **Decrypt-Methode** entschlüsselt einen Datenpuffer an Ort und Stelle.

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

Zu entschlüsselnde Daten. Wenn die Methode erfolgreich ist, werden diese Daten bei der Rückgabe entschlüsselt.

</dd> <dt>

*cbData* \[ In\]
</dt> <dd>

Größe der Daten in Bytes.

</dd> <dt>

*pWMCryptoData* \[ In\]
</dt> <dd>

Zeiger auf eine [**WMDRMCryptoData-Struktur**](wmdrmcryptodata.md) mit zusätzlichen Parametern. Kann NULL **sein,** wenn der Inhalt mit den Standardparametern verschlüsselt wurde.

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

[**IWMDRMDecrypt-Schnittstelle**](iwmdrmdecrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





