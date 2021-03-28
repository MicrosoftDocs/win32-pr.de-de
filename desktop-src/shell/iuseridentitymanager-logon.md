---
description: 'Iuseridentitymanager:: die Anmeldung wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.'
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: 'Iuseridentitymanager:: Logon-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eee6e0555d45d3f52173fce085d19c14f2ccfe8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127829"
---
# <a name="iuseridentitymanagerlogon-method"></a>Iuseridentitymanager:: Logon-Methode

\[**Iuseridentitymanager:: die Anmeldung** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Zeigt dem Benutzer eine Benutzeroberfläche an und ermöglicht dem Benutzer die Auswahl einer Benutzeridentität. Bei erfolgreicher Ausführung wird die Benutzeridentität angemeldet und abgerufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Typ: **HWND**

Ein **HWND** -Wert, der ein Fenster identifiziert, das nach dem verwerfen der Anmelde Benutzeroberfläche in den Vordergrund gestellt wird.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Typ: **DWORD**

Optionale Flags, um zu definieren, wie sich die Benutzeroberfläche verhält. Legen Sie auf UIL \_ Force UI fest, \_ um die Anzeige der Benutzeroberfläche zu erzwingen, auch wenn bereits eine Identität ausgewählt wurde.

</dd> <dt>

*ppIdentity* \[ vorgenommen\]
</dt> <dd>

Type: **[ **iuseridentity**](iuseridentity.md)\*\***

Die Adresse des Zeigers, der die ausgewählte Benutzeridentität empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Das Ergebnis des Anmeldevorgangs. Bei erfolgreicher Ausführung wird S OK zurückgegeben \_ . Andernfalls wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                            | Beschreibung                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**E- \_ Benutzer \_ abgebrochen**</dt> </dl>      | Der Benutzer hat den Anmeldevorgang von der Benutzeroberfläche abgebrochen.<br/>                               |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>          | Die Benutzeridentität konnte nicht erstellt werden.<br/>                                          |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>           | Unerwarteter Vorgang.<br/>                                               |
| <dl> <dt>**E- \_ Identitäten \_ deaktiviert**</dt> </dl> | Die Identitätsverwaltung ist im System deaktiviert.<br/>                                   |
| <dl> <dt>**S- \_ Identitäten \_ deaktiviert**</dt> </dl> | Die Identitätsverwaltung ist im System deaktiviert.<br/>                                   |
| <dl> <dt>**E \_ Identität \_ ändern**</dt> </dl>   | Das System wechselt momentan zum Wechseln von Identitäten und kann den Vorgang nicht durchführen.<br/> |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iuseridentitymanager**](iuseridentitymanager.md)
</dt> <dt>

[**Iuseridentitymanager:: abmelden**](iuseridentitymanager-logoff.md)
</dt> <dt>

[**Iuseridentitymanager:: manageidentities**](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




