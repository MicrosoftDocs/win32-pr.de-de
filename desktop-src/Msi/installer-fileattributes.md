---
description: Die FileAttributes-Eigenschaft des Installer-Objekts gibt eine Zahl zurück, die die kombinierten Dateiattribute für den angegebenen Pfad zu einer Datei oder einem Ordner darstellt.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Installer.FileAttributes-Eigenschaft (Windows.storage.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7fe43028d856ca26b1c5e8fa21a88a3b77381670ccc044a79f10d3b922f38c21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630913"
---
# <a name="installerfileattributes-property"></a>Installer.FileAttributes (Eigenschaft)

Die **FileAttributes-Eigenschaft** des [**Installer-Objekts**](installer-object.md) gibt eine Zahl zurück, die die kombinierten Dateiattribute für den angegebenen Pfad zu einer Datei oder einem Ordner darstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a>Eigenschaftswert

Der erforderliche Pfad zur Datei oder zum Ordner. Bei einem partiellen Pfad wird das aktuelle Verzeichnis angenommen.

## <a name="remarks"></a>Hinweise

Die **FileAttributes-Eigenschaft** gibt die folgenden Werte zurück.



| Dateiattribut              | Wert      | Wert |
|-----------------------------|------------|-------|
| FILE\_ATTRIBUTE\_READONLY   | 0x00000001 | 1     |
| FILE\_ATTRIBUTE\_HIDDEN     | 0x00000002 | 2     |
| FILE\_ATTRIBUTE\_SYSTEM     | 0x00000004 | 4     |
| FILE\_ATTRIBUTE\_DIRECTORY  | 0x00000010 | 16    |
| FILE \_ ATTRIBUTE \_ TEMPORARY  | 0x00000100 | 256   |
| FILE\_ATTRIBUTE\_COMPRESSED | 0x00000800 | 2048  |
| FILE\_ATTRIBUTE\_OFFLINE    | 0x00001000 | 4096  |



 

Gibt –1 zurück, wenn die Datei oder der Ordner nicht vorhanden oder nicht zugänglich ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| Header<br/>  | <dl> <dt>Windows.storage.h</dt> </dl>                                                                                                                                                            |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



 

 




