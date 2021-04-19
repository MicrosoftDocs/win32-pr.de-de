---
title: Iwmdrmlicense-Methode "| ateverschlüsseltor" (wmdrmsdk. h)
description: Die Methode "kreateverschlüsseltor" erstellt mithilfe der Einstellungen der aktuellen Lizenz ein Verschlüsselungs Objekt.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- Methode "Windows Media" der Methode "Methode"
- Kreateverschlüsseltor-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, Methode "kreateverschlüsseltor"
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
ms.openlocfilehash: 8031f412129f1d02cc4ef37c6af5f49a6c0b7532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361515"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a>Iwmdrmlicense:: up-Verschlüsselungsmethode

Die Methode " **kreateverschlüsseltor** " erstellt mithilfe der Einstellungen der aktuellen Lizenz ein Verschlüsselungs Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *ppcryptor* \[ " vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iwmdrmencrypt**](iwmdrmencrypt.md) -Schnittstelle des neu erstellten Objekts.

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

[**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[**Iwmdrmlicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





