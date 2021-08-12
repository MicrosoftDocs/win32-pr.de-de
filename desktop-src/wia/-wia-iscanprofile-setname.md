---
description: Legt den Anzeigenamen des Profils fest.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: IScanProfile::SetName-Methode (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 0023353f298d5b6690345d559517c3840d33da6eb836c983b85924b5c4ac4260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441476"
---
# <a name="iscanprofilesetname-method"></a>IScanProfile::SetName-Methode

Legt den Anzeigenamen des Profils fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrName* \[ In\]
</dt> <dd>

Typ: **BSTR**

Der Anzeigename des Profils.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode ist erforderlich, da die GUID eines Profils nicht zum Anzeigen des Überprüfungsprofils für einen Benutzer verwendet werden kann.

Ein Benutzer kann den Anzeigenamen eines Profils mit der [**ScanProfileDialog-Methode**](-wia-iscanprofileui-scanprofiledialog.md) ändern.

Änderungen an einem Profil werden erst auf dem Datenträger gespeichert, wenn die Anwendung die [**IScanProfile::Save-Methode aufruft.**](-wia-iscanprofile-save.md)

Wenn zwei Anwendungen Scanprofilobjekte aus derselben XML-Datei erstellen und jede Anwendung Änderungen in ihr -Objekt schreibt, werden nur die Änderungen, die von der Anwendung vorgenommen werden, die [**IScanProfile::Save last aufruft,**](-wia-iscanprofile-save.md) auf dem Datenträger gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



 

 




