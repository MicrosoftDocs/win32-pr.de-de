---
description: Legt die GUID der Kategorie des Windows-Abbild Erwerbs (WIA) 2,0-Elements fest, dem das Profil zugeordnet ist.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: 'Iscanprofile:: SetItem-Methode (Scanprofile. h)'
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
ms.openlocfilehash: d4b20aae0740656b46dd26824947fc27513afcac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354533"
---
# <a name="iscanprofilesetitem-method"></a>Iscanprofile:: SetItem-Methode

Legt die GUID der Kategorie des Windows-Abbild Erwerbs (WIA) 2,0-Elements fest, dem das Profil zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*guidcategory* \[ in\]
</dt> <dd>

Typ: **GUID**

Die GUID der Kategorie des WIA 2,0-Elements. Dabei muss es sich um eine der WIA- \_ IPA- \_ Element Kategorie- \_ Konstanten handeln.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Benutzer können die Kategorie mit der [**scanprofiledialog**](-wia-iscanprofileui-scanprofiledialog.md) -Methode ändern.

Änderungen an einem Profil werden erst auf dem Datenträger gespeichert, wenn die Anwendung die [**iscanprofile:: Save**](-wia-iscanprofile-save.md) -Methode aufruft.

Wenn zwei Anwendungen Überprüfungs Profil Objekte aus derselben XML-Datei erstellen und jede Anwendung Änderungen in das zugehörige Objekt schreibt, werden nur die Änderungen, die von der Anwendung vorgenommen werden, die [**iscanprofile:: Save**](-wia-iscanprofile-save.md) Last aufruft, auf dem Datenträger gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscanprofile**](-wia-iscanprofile.md)
</dt> <dt>

[Profil Schema überprüfen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




