---
title: Iwmdrmencryptscatter-Verschlüsselungsmethode (wmdrmsdk. h)
description: Die verschlüsselungsscatter-Methode entkratzt und verschlüsselt Daten.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Verschlüsseltscatter-Methode Windows Media-Format
- Verschlüsseltscatter-Methode Windows Media-Format, iwmdrmencryptscatter-Schnittstelle
- Iwmdrmencryptscatter-Schnittstelle Windows Media-Format, verschlüsseltscatter-Methode
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
ms.openlocfilehash: 58b2d1d6182aed55b60aa1cedfbce5dd870691bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369526"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a>Iwmdrmencryptscatter:: verschlüsseltscatter-Methode

Die **verschlüsselungsscatter** -Methode entkratzt und verschlüsselt Daten.

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

*cblocks* \[ in\]
</dt> <dd>

Anzahl der Elemente im *rgblocks* -Array.

</dd> <dt>

*rgblocks* \[ in\]
</dt> <dd>

Array von mindestens einer [**WMDRM- \_ Verschlüsselungs \_ Punkt \_ Block**](wmdrm-encrypt-scatter-block.md) Struktur. Jedes Element beschreibt einen Datenblock, der entfernt und verschlüsselt werden soll.

</dd> <dt>

*pwmcryptodata* \[ in\]
</dt> <dd>

Zeiger auf eine [**wmdrmcryptodata**](wmdrmcryptodata.md) -Struktur, die Verschlüsselungs Parameter enthält. Legen Sie auf **null** fest, um die Standardparameter zu verwenden.

</dd> <dt>

*cboutput* \[ in\]
</dt> <dd>

Die Größe des Ausgabedaten Puffers, der als *pboutput* übergeben wird.

</dd> <dt>

*pboutput* \[ vorgenommen\]
</dt> <dd>

Ausgabepuffer.

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

[**Initencryptscatter**](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[**Iwmdrmencryptscatter-Schnittstelle**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





