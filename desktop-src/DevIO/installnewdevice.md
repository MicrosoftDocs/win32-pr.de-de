---
description: Installiert ein neues Gerät. Der Benutzer wird aufgefordert, das Gerät auszuwählen.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: Installnewdevice-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: 76a458ae071c61b9f1030aad535c4d4c6a31078c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127289"
---
# <a name="installnewdevice-function"></a>Installnewdevice-Funktion

Installiert ein neues Gerät. Der Benutzer wird aufgefordert, das Gerät auszuwählen.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Ein Handle für das Fenster auf oberster Ebene, das für jede erforderliche Benutzeroberfläche verwendet werden soll.

</dd> <dt>

*Klassen-GUID* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Klassen- **GUID**. Dieser Parameter ist optional. Wenn dieser Parameter **null** ist, wird der Benutzer auf der Seite zur Auswahl der Erkennung gestartet. Wenn es sich bei diesem Parameter um **GUID \_ null** oder **GUID \_ DEVCLASS \_ Unknown** handelt, wird der Benutzer auf der Seite Klassenauswahl gestartet.

</dd> <dt>

*vorab Start* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die den Neustart Status empfängt. Dieser Parameter kann " **di \_ needrestart** " oder " **di \_ NEEDREBOOT**" lauten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Sie müssen die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit NewDev.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                        |
| DLL<br/>                      | <dl> <dt>NewDev.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Geräte Verwaltungsfunktionen](device-management-functions.md)
</dt> </dl>

 

