---
description: Die Filesize-Methode des Installer-Objekts verwendet Win32-API-Aufrufe, um die Größe der in path angegebenen Datei zurückzugeben.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Installer. Filesize-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 593319b88e3942ae6caa1399adbe2e596bf6e737
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369551"
---
# <a name="installerfilesize-method"></a>Installer. Filesize-Methode

Die **FileSize** -Methode des [**Installer**](installer-object.md) -Objekts verwendet Win32-API-Aufrufe, um die Größe der in *path* angegebenen Datei zurückzugeben.

## <a name="syntax"></a>Syntax


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* 
</dt> <dd>

Erforderliche Zeichenfolge, die den Pfad zur Datei enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




