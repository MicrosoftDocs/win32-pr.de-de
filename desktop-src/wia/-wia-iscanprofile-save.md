---
description: Speichert Änderungen an einem Profil auf der Festplatte.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: 'Iscanprofile:: Save-Methode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 6d4787380344a7bf8adb70f4cb5a3eaacdea403a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527086"
---
# <a name="iscanprofilesave-method"></a>Iscanprofile:: Save-Methode

Speichert Änderungen an einem Profil auf der Festplatte.

## <a name="syntax"></a>Syntax


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Bei einem gespeicherten Überprüfungs Profil handelt es sich um eine XML-Datei, die unter% User Profile% \\ Application Data \\ Microsoft \\ Document Center \\ userscanprofiles gespeichert ist.

Wenn mehr als ein Prozess in das [**iscanprofile**](-wia-iscanprofile.md) -Objekt schreibt, ist das Objekt, das **iscanprofile:: Save** Last aufruft, der einzige Prozess, dessen Änderungen gespeichert werden.

Die **iscanprofile:: Save** -Methode überprüft das Profil vor dem Speichern. Das Profil wird immer als gültig angesehen, es sei denn, die Kategorie des Windows-Abbild Erwerbs (WIA) 2,0-Elements, das mit dem Profil verknüpft ist, ist entweder eine Kategorie mit einem \_ \_ Flatbed oder eine \_ Kategorie- \_ Feed Wenn es sich bei der Kategorie um eine Kategorie vom Typ " \_ Kategorie für \_ flatgrades" oder um einen \_ kategorieanleger handelt \_ , müssen die folgenden Eigenschaften für das Element gültig sein, wenn die Eigenschaften im Profil enthalten sind:

Helligkeit der WIA- \_ IPS \_

Kontrast zwischen WIA- \_ IPS \_

WIA \_ IPA- \_ DataType

WIA- \_ IPS- \_ xres

WIA \_ IPA- \_ Format

Wenn es sich bei der Kategorie um einen "a category"-Wert handelt \_ \_ , muss die Eigenschaft "WIA \_ IPS page size" ggf \_ \_ . gültig sein, wenn Sie im Profil vorhanden ist. Weitere Informationen zu diesen Eigenschaften finden Sie unter [**Scanner WIA Item Property Konstanten**](-wia-wiaitempropscanneritem.md).

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

 

 




