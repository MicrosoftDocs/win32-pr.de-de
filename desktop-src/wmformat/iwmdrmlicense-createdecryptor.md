---
title: IWMDRMLicense CreateDecryptor-Methode (Wmdrmsdk.h)
description: Die CreateDecryptor-Methode erstellt ein Entschlüsselungsobjekt mithilfe der Einstellungen der aktuellen Lizenz.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- CreateDecryptor-Methode windows Media Format
- CreateDecryptor-Methode windows Media Format , IWMDRMLicense-Schnittstelle
- IWMDRMLicense-Schnittstelle windows Media Format , CreateDecryptor-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ac7e6bb1e9d4f9e5e7c706c0a9e3518f62b1068ed743dc795554dd43ac61e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027708"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a>IWMDRMLicense::CreateDecryptor-Methode

Die **CreateDecryptor-Methode** erstellt ein Entschlüsselungsobjekt mithilfe der Einstellungen der aktuellen Lizenz.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDecryptor* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IWMDRMDecrypt-Schnittstelle**](iwmdrmdecrypt.md) des neu erstellten Objekts.

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

[**CreateEncryptor**](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[**IWMDRMLicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





