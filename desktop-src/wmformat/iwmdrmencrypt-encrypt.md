---
title: IWMDRMEncrypt Encrypt-Methode (Wmdrmsdk.h)
description: Die Encrypt-Methode verschlüsselt einen Datenpuffer an Ort und Stelle.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Encrypt method windows Media Format
- Encrypt method windows Media Format , IWMDRMEncrypt interface
- IWMDRMEncrypt-Schnittstelle Windows Media Format , Encrypt-Methode
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb49b2857c23bb11b5e4d091dece820bb833b2b4e77224558f2d7972885445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027738"
---
# <a name="iwmdrmencryptencrypt-method"></a>IWMDRMEncrypt::Encrypt-Methode

Die **Encrypt-Methode** verschlüsselt einen Datenpuffer an Ort und Stelle.

## <a name="syntax"></a>Syntax


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbData* \[ in, out\]
</dt> <dd>

Zu verschlüsselnde Daten. Wenn die Methode erfolgreich ist, werden die Daten bei der Rückgabe verschlüsselt.

</dd> <dt>

*cbData* \[ In\]
</dt> <dd>

Größe der Daten in Bytes.

</dd> <dt>

*pWMCryptoData* \[ In\]
</dt> <dd>

Zeiger auf eine [**WMDRMCryptoData-Struktur**](wmdrmcryptodata.md) mit zusätzlichen Parametern. Legen Sie auf **NULL fest,** um die Standardverschlüsselungswerte zu verwenden.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMEncrypt-Schnittstelle**](iwmdrmencrypt.md)
</dt> <dt>

[**WMDRMCryptoData**](wmdrmcryptodata.md)
</dt> </dl>

 

 





