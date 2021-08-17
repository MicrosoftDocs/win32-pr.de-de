---
description: Die InstallWiaDevice-Funktion installiert ein WIA-Gerät (Windows Image Acquisition) als stammbasiertes Gerät. Es wird möglicherweise eine Sicherheitswarnung angezeigt, wenn eine installierte Datei oder ein Coinstaller nicht digital signiert und vertrauenswürdig ist.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: InstallWiaDevice-Funktion (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallWiaDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 10006e234c9a76054a77fb64f89a31d9a21e394066bcc98813912bad9f804e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965839"
---
# <a name="installwiadevice-function"></a>InstallWiaDevice-Funktion

Die **InstallWiaDevice-Funktion** installiert ein WIA-Gerät (Windows Image Acquisition) als root-enumeriertes Gerät. Es wird möglicherweise eine Sicherheitswarnung angezeigt, wenn eine installierte Datei oder ein Coinstaller nicht digital signiert und vertrauenswürdig ist.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWiaDeviceInstall* \[ In\]
</dt> <dd>

Typ: **PWIADEVICEINSTALL \***

Zeiger auf eine WIADEVICEINSTALL-Struktur. Der *szFriendlyName-Member* der -Struktur muss auf den tatsächlichen FriendlyName des Geräts festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **DWORD**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, wird ein Win32-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




