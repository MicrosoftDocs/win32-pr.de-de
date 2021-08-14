---
description: Installiert ein neues Gerät. Der Benutzer wird aufgefordert, das Gerät auszuwählen.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: InstallNewDevice-Funktion
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
ms.openlocfilehash: cb12e87ceee4812ffc8c0e39d961ce631e26c4ab8ca7ae555785c8ad8381ca01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405307"
---
# <a name="installnewdevice-function"></a>InstallNewDevice-Funktion

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

*hwndParent* \[ In\]
</dt> <dd>

Ein Handle für das Fenster der obersten Ebene, das für alle erforderlichen Benutzeroberflächen verwendet werden soll.

</dd> <dt>

*ClassGuid* \[ In\]
</dt> <dd>

Ein Zeiger auf eine **Klassen-GUID.** Dieser Parameter ist optional. Wenn dieser Parameter **NULL** ist, beginnt der Benutzer auf der Auswahlseite für die Erkennung. Wenn dieser Parameter **GUID \_ NULL** oder **GUID \_ DEVCLASS \_ UNKNOWN** ist, beginnt der Benutzer auf der Seite zur Klassenauswahl.

</dd> <dt>

*pReboot* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die den Neustartstatus empfängt. Dieser Parameter kann **DI \_ NEEDRESTART** oder **DI \_ NEEDREBOOT** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Importbibliothek zugeordnet. Sie müssen die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch mit NewDev.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                        |
| DLL<br/>                      | <dl> <dt>NewDev.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Geräteverwaltung Functions](device-management-functions.md)
</dt> </dl>

 

