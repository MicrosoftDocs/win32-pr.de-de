---
description: Legt die GUID der Kategorie des Elements Windows Image Acquisition (WIA) 2.0 fest, dem das Profil zugeordnet ist.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: IScanProfile::SetItem-Methode (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: fc4f79c44ff84bef1efbda4b09beee6b7dcf83f04023a5e2211e9f808b18446a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814070"
---
# <a name="iscanprofilesetitem-method"></a>IScanProfile::SetItem-Methode

Legt die GUID der Kategorie des Elements Windows Image Acquisition (WIA) 2.0 fest, dem das Profil zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*guidCategory* \[ In\]
</dt> <dd>

Typ: **GUID**

Die GUID der Kategorie des WIA 2.0-Elements. Dies muss eine der WIA \_ IPA \_ ITEM \_ CATEGORY-Konstanten sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Benutzer können die Kategorie mit der [**ScanProfileDialog-Methode**](-wia-iscanprofileui-scanprofiledialog.md) ändern.

Änderungen an einem Profil werden erst auf dem Datenträger gespeichert, wenn die Anwendung die [**IScanProfile::Save-Methode aufruft.**](-wia-iscanprofile-save.md)

Wenn zwei Anwendungen Scanprofilobjekte aus derselben XML-Datei erstellen und jede Anwendung Änderungen in ihr -Objekt schreibt, werden nur die Änderungen, die von der Anwendung vorgenommen werden, die [**IScanProfile::Save last aufruft,**](-wia-iscanprofile-save.md) auf dem Datenträger gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Scanprofilschema](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




