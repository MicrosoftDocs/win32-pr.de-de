---
description: Erstellt ein Benutzerprofil für einen angegebenen Benutzer.
ms.assetid: e4ea4032-d8d3-45c1-b2e5-7fef52a8a869
title: Funktion "feateuserprofileex"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateUserProfileEx
- CreateUserProfileExA
- CreateUserProfileExW
api_type:
- DllExport
api_location:
- Userenv.dll
ms.openlocfilehash: 8dbb76293fda769ec720221ca1bfa4474af1620c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982948"
---
# <a name="createuserprofileex-function"></a>Funktion "feateuserprofileex"

\[Diese Funktion ist ab Windows Vista nicht verfügbar.\]

Erstellt ein Benutzerprofil für einen angegebenen Benutzer.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CreateUserProfileEx(
  _In_      PSID    pSid,
  _In_      LPCTSTR lpUserName,
  _In_opt_  LPCTSTR lpUserHive,
  _Out_opt_ LPTSTR  lpProfileDir,
  _In_      DWORD   dwDirSize,
  _In_      BOOL    bWin9xUpg
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PSID* \[ in\]
</dt> <dd>

Typ: **PSID**

Die SID des neuen Benutzers.

</dd> <dt>

*lpusername* \[ in\]
</dt> <dd>

Typ: **LPCTSTR**

Zeiger auf einen Puffer, der den Benutzernamen des neuen Benutzers enthält.

</dd> <dt>

*lpuserhive* \[ in, optional\]
</dt> <dd>

Typ: **LPCTSTR**

Zeiger auf einen Puffer, der die zu verwendende [Registrierungs](../sysinfo/registry-hives.md) Struktur enthält. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lpprofiledir* \[ Out, optional\]
</dt> <dd>

Typ: **LPTSTR**

Ein Zeiger auf einen Puffer, der, wenn diese Funktion zurückgibt, den Profilverzeichnis Pfad des Benutzers empfängt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*dwdirsize* \[ in\]
</dt> <dd>

Typ: **DWORD**

Größe des Puffers, der von *lpprofiledir* in tchars angegeben wird.

</dd> <dt>

*bWin9xUpg* \[ in\]
</dt> <dd>

Typ: **bool**

**True** , wenn das Benutzerprofil im Rahmen einer Profil Migration von Windows 9X erstellt wird. andernfalls **false**.

Wenn der Wert **true** ist, wird das Benutzerprofil im Standardprofil Verzeichnis – normalerweise C: \\ Dokumente und Einstellungen \\ *username* festgelegt. Wenn dieses Verzeichnis bereits vorhanden ist, wird es verwendet. Wenn dies nicht der Fall ist, wird Sie erstellt.

Wenn der Wert **false** ist, wird das Standardprofil Verzeichnis erstellt, wenn es nicht vorhanden ist. Wenn das Standardprofil Verzeichnis bereits vorhanden ist, wird ein neues Verzeichnis für dieses Benutzerprofil erstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **bool**

Gibt **true** zurück, wenn das neue Benutzerprofil erfolgreich erstellt wurde. andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist nicht in den Software Development Kit-Headern (SDK) deklariert und verfügt über keine zugeordnete Import Bibliothek. Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um mit Userenv.dll zu verknüpfen. Auf die ANSI-Version der Funktion, auf die die Funktion " **kreateuserprofileexa" verweist** , wird von Userenv.dll als Ordnungszahl 153 verwiesen. Auf die Unicode-Version, " **kreateuserprofileexw** ", wird als Ordnungszahl 154 verwiesen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/>  | Windows XP<br/>                                                                  |
| DLL<br/>                    | <dl> <dt>Userenv.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/> | " **Samateuserprofileexw** " (Unicode) und " **kreateuserprofileexa** " (ANSI)<br/>      |



 

 
