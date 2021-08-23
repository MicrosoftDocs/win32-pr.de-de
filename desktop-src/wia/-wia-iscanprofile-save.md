---
description: Speichert Änderungen an einem Profil auf dem Datenträger.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: IScanProfile::Save-Methode (Scanprofile.h)
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
ms.openlocfilehash: 7cf4201a0d149c7b529e595d7f2c2ea92a6010f6cffd3e6c5c74fb3cdc040651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450920"
---
# <a name="iscanprofilesave-method"></a>IScanProfile::Save-Methode

Speichert Änderungen an einem Profil auf dem Datenträger.

## <a name="syntax"></a>Syntax


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Ein gespeichertes Scanprofil ist eine XML-Datei, die unter %USERPROFILE% \\ Application Data Microsoft Document Center \\ \\ \\ UserScanProfiles gespeichert ist.

Wenn mehr als ein Prozess in das [**IScanProfile-Objekt**](-wia-iscanprofile.md) schreibt, ist der Prozess, der **IScanProfile::Save last aufruft,** der einzige Prozess, dessen Änderungen gespeichert werden.

Die **IScanProfile::Save-Methode** überprüft das Profil vor dem Speichern. Das Profil gilt immer als gültig, es sei denn, die Kategorie des elements Windows Image Acquisition (WIA) 2.0, das dem Profil zugeordnet ist, ist entweder WIA \_ CATEGORY \_ FLATBED oder WIA \_ CATEGORY \_ FEEDER. Wenn die Kategorie WIA \_ CATEGORY \_ FLATBED oder WIA \_ CATEGORY \_ FEEDER ist, müssen die folgenden Eigenschaften für das Element gültig sein, wenn die Eigenschaften im Profil enthalten sind:

WIA \_ \_ IPS-HELLIGKEIT

\_WIA-IPS-KONTRAST \_

WIA \_ \_ IPA-DATENTYP

WIA \_ IPS \_ XRES

WIA \_ \_ IPA-FORMAT

Wenn es sich bei der Kategorie um WIA \_ CATEGORY \_ FEEDER handelt, muss die \_ WIA IPS PAGE \_ \_ SIZE-Eigenschaft gültig sein, sofern sie im Profil vorhanden ist. Weitere Informationen zu diesen Eigenschaften finden Sie unter [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Scanprofilschema](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




