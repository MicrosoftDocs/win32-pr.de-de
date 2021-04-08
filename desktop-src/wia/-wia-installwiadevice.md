---
description: Die installwiadevice-Funktion installiert ein Windows-Abbild Erfassungsgerät (WIA) als von der Stamm-Enumeration erfasste Geräte. Möglicherweise wird eine Sicherheitswarnung angezeigt, wenn eine Installationsdatei oder ein installiertes Coinstaller nicht digital signiert und vertrauenswürdig ist.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Installwiadevice-Funktion (WIA. h)
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
ms.openlocfilehash: 62060d538b4b51fe22e10df09093f1f7f8c26a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752864"
---
# <a name="installwiadevice-function"></a>Installwiadevice-Funktion

Die **installwiadevice** -Funktion installiert ein Windows-Abbild Erfassungsgerät (WIA) als von der Stamm-Enumeration erfasste Geräte. Möglicherweise wird eine Sicherheitswarnung angezeigt, wenn eine Installationsdatei oder ein installiertes Coinstaller nicht digital signiert und vertrauenswürdig ist.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwiadeviceingestall* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **pwiadeviceinstall \** _

Zeiger auf eine wiadeviceingestall-Struktur. Der _szFriendlyName *-Member der-Struktur muss auf den tatsächlichen Geräte FriendlyName festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **DWORD**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, wird ein Win32-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




