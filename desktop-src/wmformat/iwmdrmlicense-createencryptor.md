---
title: IWMDRMLicense CreateEncryptor-Methode (Wmdrmsdk.h)
description: Die CreateEncryptor-Methode erstellt ein Verschlüsselungsobjekt mithilfe der Einstellungen der aktuellen Lizenz.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- CreateEncryptor-Methode windows Media Format
- CreateEncryptor-Methode windows Media Format , IWMDRMLicense-Schnittstelle
- IWMDRMLicense-Schnittstelle windows Media Format , CreateEncryptor-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481e33b6a3d4ffff3805ccc14f45b06a12ad2296fdaaedf13608f3a519c6ed10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433659"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a>IWMDRMLicense::CreateEncryptor-Methode

Die **CreateEncryptor-Methode** erstellt ein Verschlüsselungsobjekt mithilfe der Einstellungen der aktuellen Lizenz.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEncryptor* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IWMDRMEncrypt-Schnittstelle**](iwmdrmencrypt.md) des neu erstellten Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                | Beschreibung                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ \_ DRM- WIES ZU \_ \_ KLEIN**</dt> </dl> | Eine aktualisierte Inhaltssperrliste ist erforderlich.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[**IWMDRMLicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





