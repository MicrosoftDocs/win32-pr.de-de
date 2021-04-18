---
title: Iwmdrmencrypt-Verschlüsselungsmethode (wmdrmsdk. h)
description: Die Methode "verschlüsseln" verschlüsselt einen Datenpuffer an Ort und Stelle.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Verschlüsselungsmethode (Windows Media-Format)
- Verschlüsseln der Methode Windows Media-Format, iwmdrmencrypt-Schnittstelle
- Iwmdrmencrypt-Schnittstelle Windows Media-Format, Methode verschlüsseln
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
ms.openlocfilehash: 13380b321b540cbb5edce3c03e422b49c7b90e54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365385"
---
# <a name="iwmdrmencryptencrypt-method"></a>Iwmdrmencrypt:: Verschlüsseln-Methode

Die Methode " **verschlüsseln** " verschlüsselt einen Datenpuffer an Ort und Stelle.

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

Die zu verschlüsselnden Daten. Wenn die Methode erfolgreich ausgeführt wird, werden die Daten bei der Rückgabe verschlüsselt.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Größe der Daten in Bytes.

</dd> <dt>

*pwmcryptodata* \[ in\]
</dt> <dd>

Zeiger auf eine [**wmdrmcryptodata**](wmdrmcryptodata.md) -Struktur mit zusätzlichen Parametern. Legen Sie auf **null** fest, um die Standard Verschlüsselungs Werte zu verwenden.

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

[**Iwmdrmencrypt-Schnittstelle**](iwmdrmencrypt.md)
</dt> <dt>

[**Wmdrmcryptodata**](wmdrmcryptodata.md)
</dt> </dl>

 

 





