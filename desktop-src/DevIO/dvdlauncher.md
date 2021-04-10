---
description: Überprüft, ob der Medienbereich im DVD-Laufwerk mit dem DVD-Laufwerks Bereich übereinstimmt.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: DVDLauncher-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: ef49be579052e5a9fd493f5bf246a2efbd217c34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127292"
---
# <a name="dvdlauncher-function"></a>DVDLauncher-Funktion

Überprüft, ob der Medienbereich im DVD-Laufwerk mit dem DVD-Laufwerks Bereich übereinstimmt.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Ein Handle für das Fenster auf oberster Ebene, das für jede erforderliche Benutzeroberfläche verwendet werden soll.

</dd> <dt>

Laufwerk *Etter* \[ in\]
</dt> <dd>

Der Laufwerk Buchstabe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird und die Bereiche einander entsprechen, ist der Rückgabewert ungleich 0 (null). Andernfalls ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Sie müssen die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit StorProp.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                          |
| DLL<br/>                      | <dl> <dt>StorProp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Geräte Verwaltungsfunktionen](device-management-functions.md)
</dt> </dl>

 

