---
description: Die FileSize-Methode des Installer-Objekts verwendet Win32-API-Aufrufe, um die Größe der in Path angegebenen Datei zurück anzugeben.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Installer.FileSize-Methode
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
ms.openlocfilehash: f585da776d348e7c774d4671a230881f2ec0e4ddaca8a63842d59a9b77a61972
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630689"
---
# <a name="installerfilesize-method"></a>Installer.FileSize-Methode

Die **FileSize-Methode** des [**Installer-Objekts**](installer-object.md) verwendet Win32-API-Aufrufe, um die Größe der in Pfad angegebenen Datei *zurück anzugeben.*

## <a name="syntax"></a>Syntax


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Path* 
</dt> <dd>

Erforderliche Zeichenfolge, die den Pfad zur Datei enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



 

 




