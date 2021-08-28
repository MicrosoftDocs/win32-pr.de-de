---
title: IWMDRMEncryptScatter EncryptScatter-Methode (Wmdrmsdk.h)
description: Die EncryptScatter-Methode verwirft und verschlüsselt Daten.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- EncryptScatter-Methode windows Media Format
- EncryptScatter-Methode windows Media Format , IWMDRMEncryptScatter-Schnittstelle
- IWMDRMEncryptScatter-Schnittstelle windows Media Format , EncryptScatter-Methode
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fae3f8a40bc5468898424dcf33bf947235a632db44f4dada7f2c96b2a3a064b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839710"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a>IWMDRMEncryptScatter::EncryptScatter-Methode

Die **EncryptScatter-Methode** verwirft und verschlüsselt Daten.

## <a name="syntax"></a>Syntax


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cBlocks* \[ In\]
</dt> <dd>

Anzahl der Elemente im *rgBlocks-Array.*

</dd> <dt>

*rgBlocks* \[ In\]
</dt> <dd>

Array von mindestens einer [**WMDRM \_ ENCRYPT \_ SCATTER \_ BLOCK-Struktur.**](wmdrm-encrypt-scatter-block.md) Jedes Element beschreibt einen Datenblock, der unscrambled und verschlüsselt werden soll.

</dd> <dt>

*pWMCryptoData* \[ In\]
</dt> <dd>

Zeiger auf eine [**WMDRMCryptoData-Struktur,**](wmdrmcryptodata.md) die Verschlüsselungsparameter enthält. Legen Sie diese Einstellung auf **NULL** fest, um die Standardparameter zu verwenden.

</dd> <dt>

*cbOutput* \[ In\]
</dt> <dd>

Größe des Ausgabedatenpuffers, der als *pbOutput* übergeben wird.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Ausgabepuffer.

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

[**InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[**IWMDRMEncryptScatter-Schnittstelle**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





