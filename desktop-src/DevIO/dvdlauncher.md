---
description: Überprüft, ob der Medienbereich auf dem DVD-Laufwerk dem DVD-Laufwerksbereich entspricht.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: DvdLauncher-Funktion
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
ms.openlocfilehash: a52ac620e5ec9aa3d9060d35921fcfd9c5bcc6e73cebf71ef336ceb54fc0806e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956909"
---
# <a name="dvdlauncher-function"></a>DvdLauncher-Funktion

Überprüft, ob der Medienbereich auf dem DVD-Laufwerk dem DVD-Laufwerksbereich entspricht.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWnd* \[ In\]
</dt> <dd>

Ein Handle für das Fenster der obersten Ebene, das für jede erforderliche Benutzeroberfläche verwendet werden soll.

</dd> <dt>

*DriveLetter* \[ In\]
</dt> <dd>

Der Laufwerkbuchstaben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist und die Regionen übereinstimmen, ist der Rückgabewert ungleich null. Andernfalls ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek zugeordnet. Sie müssen die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit StorProp.dll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                          |
| DLL<br/>                      | <dl> <dt>StorProp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Geräteverwaltung Functions](device-management-functions.md)
</dt> </dl>

 

