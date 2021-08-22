---
description: Ruft die GUID der Kategorie des elements Windows Image Acquisition (WIA) 2.0 ab, dem das Profil zugeordnet ist.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: IScanProfile::GetItem-Methode (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 5a7f52a2d89bbd35b59febb25528fe493c4b5646afc70251fc19978d6d6265db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451040"
---
# <a name="iscanprofilegetitem-method"></a>IScanProfile::GetItem-Methode

Ruft die GUID der Kategorie des elements Windows Image Acquisition (WIA) 2.0 ab, dem das Profil zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguidCategory* \[ out\]
</dt> <dd>

Typ: **GUID \***

Ein Zeiger auf die GUID der Kategorie des WIA 2.0-Elements. Dies ist immer eine der WIA \_ IPA \_ ITEM \_ CATEGORY-Konstanten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Scanprofilschema](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




