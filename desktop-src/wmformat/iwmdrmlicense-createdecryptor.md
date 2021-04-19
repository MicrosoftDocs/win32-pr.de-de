---
title: Iwmdrmlicense-Methode "deatedecryptor" (wmdrmsdk. h)
description: Die Methode "kreatedecryptor" erstellt mithilfe der Einstellungen der aktuellen Lizenz ein Entschlüsselungs-Objekt.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- Methode "Windows Media" der Methode "kreatedecryptor"
- Methode "deatedecryptor" Windows Media Format, iwmdrmlicense Interface
- Iwmdrmlicense-Schnittstelle Windows Media-Format, Methode "kreatedecryptor"
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
ms.openlocfilehash: e987e7ffa3390462889b128f390934f05e64cdff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353799"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a>Iwmdrmlicense:: kreatedecryptor-Methode

Die Methode " **kreatedecryptor** " erstellt mithilfe der Einstellungen der aktuellen Lizenz ein Entschlüsselungs-Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppdecryptor* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iwmdrmentschlüsseln**](iwmdrmdecrypt.md) -Schnittstelle des neu erstellten Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                | Beschreibung                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt> </dl> | Es wird eine aktualisierte Inhalts Sperr Liste benötigt.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CreateEncryptor**](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[**Iwmdrmlicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





