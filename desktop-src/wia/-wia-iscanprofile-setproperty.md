---
description: Legt den Wert der angegebenen untergeordneten Eigenschaften in fest. <Properties> -Element eines Scanprofils.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: IScanProfile::SetProperty-Methode (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: ba4c7aff5139f1230179299d80065f1b933a6cf2d01d4ca03c045ccbe142c3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441426"
---
# <a name="iscanprofilesetproperty-method"></a>IScanProfile::SetProperty-Methode

Legt den Wert der angegebenen untergeordneten Eigenschaften im `<Properties>` -Element eines Scanprofils fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*num* \[ In\]
</dt> <dd>

Typ: **ULONG**

Die Anzahl der Einträge in den Arrays, auf die *pid* und *pvar* verweisen.

</dd> <dt>

*Pid* \[ In\]
</dt> <dd>

Typ: **PROPID \***

Ein Zeiger auf ein Array von Identifikationsnummern der festzulegenden Eigenschaften. Jeder Wert im Array ist eine [WIA-Eigenschaftskonstante.](-wia-wia-property-constants.md)

</dd> <dt>

*pvar* \[ In\]
</dt> <dd>

Typ: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\***

Ein Zeiger auf ein Array von Werten, die den Eigenschaften zugewiesen werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Jeder Wert im Array, auf den *pid* zeigt, ist eine der [WIA-Eigenschaftskonstanten.](-wia-wia-property-constants.md) Sie können dieses Identifikationssystem erweitern. Weitere Informationen finden Sie unter [Definieren von benutzerdefinierten Eigenschaften.](-wia-defining-custom-properties.md)

Änderungen an einem Profil werden erst auf dem Datenträger gespeichert, wenn die Anwendung die [**IScanProfile::Save-Methode aufruft.**](-wia-iscanprofile-save.md)

Wenn zwei Anwendungen Scanprofilobjekte aus derselben XML-Datei erstellen und jede Anwendung Änderungen in ihr -Objekt schreibt, werden nur die Änderungen, die von der Anwendung vorgenommen werden, die [**IScanProfile::Save last aufruft,**](-wia-iscanprofile-save.md) auf dem Datenträger gespeichert.

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

**Konzeptionellen**
</dt> <dt>

[Scanprofilschema](-wia-scan-profile-schema.md)
</dt> <dt>

[WIA-Eigenschaftenkonstanten](-wia-wia-property-constants.md)
</dt> <dt>

[Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
