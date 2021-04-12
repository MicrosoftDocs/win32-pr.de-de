---
description: Zeigt ein Dialogfeld an, in dem Benutzer Scan Profile erstellen, ändern und löschen können.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'Iscanprofileui:: scanprofiledialog-Methode (scanprofileui. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: bc8707378f1debc322fea258ceb8aad0c6400ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216051"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a>Iscanprofileui:: scanprofiledialog-Methode

Zeigt ein Dialogfeld an, in dem Benutzer Scan Profile erstellen, ändern und löschen können.

## <a name="syntax"></a>Syntax


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Typ: **HWND**

Das Handle des übergeordneten Fensters, das das Dialogfeld besitzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Das Dialogfeld ist modal. der Benutzer kann erst zum übergeordneten Fenster wechseln, wenn das Dialogfeld geschlossen wird.

Die Werte des `<ProfileName>` -Elements und des- `<WiaItem>` Elements können im Dialogfeld geändert werden. Das- `<Default>` Element kann hinzugefügt oder gelöscht werden. Im Dialogfeld können keine anderen Änderungen am Überprüfungs Profil vorgenommen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofileui. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscanprofileui**](-wia-iscanprofileui.md)
</dt> <dt>

[Profil Schema überprüfen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




