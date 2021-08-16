---
description: Zeigt ein Dialogfeld an, in dem Benutzer Scanprofile erstellen, ändern und löschen können.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: IScanProfileUI::ScanProfileDialog-Methode (Scanprofileui.h)
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
ms.openlocfilehash: a2003471a151677b5f0fbd9ae88e9d3cf8d975525a9dbf8340c6fc1a9f2befc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965809"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a>IScanProfileUI::ScanProfileDialog-Methode

Zeigt ein Dialogfeld an, in dem Benutzer Scanprofile erstellen, ändern und löschen können.

## <a name="syntax"></a>Syntax


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ In\]
</dt> <dd>

Typ: **HWND**

Das Handle des übergeordneten Fensters, das das Dialogfeld besitzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Das Dialogfeld ist modal. Der Benutzer kann erst zum übergeordneten Fenster wechseln, wenn das Dialogfeld geschlossen wird.

Die Werte des `<ProfileName>` -Elements und des `<WiaItem>` -Elements können im Dialogfeld geändert werden. Das `<Default>` Element kann hinzugefügt oder gelöscht werden. Im Dialogfeld können keine weiteren Änderungen am Scanprofil vorgenommen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofileui.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IScanProfileUI**](-wia-iscanprofileui.md)
</dt> <dt>

[Scanprofilschema](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




