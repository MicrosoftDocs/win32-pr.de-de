---
description: Ruft die Anzahl der Scan Profile für das Gerät ab.
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: 'Iscanprofilemgr:: getnumprofilesfordeviceid-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 1a65e1f6571f4ec12a9bd91749c7419f9f9641c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214830"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a>Iscanprofilemgr:: getnumprofilesfordeviceid-Methode

Ruft die Anzahl der Scan Profile für das Gerät ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstraude viceid* \[ in\]
</dt> <dd>

Typ: **BSTR**

Die ID des Geräts.

</dd> <dt>

*pulnumprofiles* \[ vorgenommen\]
</dt> <dd>

Typ: **ulong \** _

Ein Zeiger auf die Anzahl der für das Gerät verfügbaren Profile.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscanprofilemgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Profil Schema überprüfen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




