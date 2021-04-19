---
description: Die File Attributeigenschaft des Installer-Objekts gibt eine Zahl zurück, die die kombinierten Dateiattribute für den angegebenen Pfad zu einer Datei oder einem Ordner darstellt.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Installer. File Attribute-Eigenschaft (Windows. Storage. h)
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
ms.openlocfilehash: e9a4d2b956c7d325fabcda7d6950274249120a0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369379"
---
# <a name="installerfileattributes-property"></a>Installer. File Attribute (Eigenschaft)

Die **File Attributeigenschaft** des [**Installer**](installer-object.md) -Objekts gibt eine Zahl zurück, die die kombinierten Dateiattribute für den angegebenen Pfad zu einer Datei oder einem Ordner darstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a>Eigenschaftswert

Der erforderliche Pfad zur Datei oder zum Ordner. Ein partieller Pfad nimmt das aktuelle Verzeichnis an.

## <a name="remarks"></a>Bemerkungen

Die **File Attributeigenschaft** gibt die folgenden Werte zurück.



| File-Attribut              | Wert      | Wert |
|-----------------------------|------------|-------|
| FILE\_ATTRIBUTE\_READONLY   | 0x00000001 | 1     |
| FILE\_ATTRIBUTE\_HIDDEN     | 0x00000002 | 2     |
| FILE\_ATTRIBUTE\_SYSTEM     | 0x00000004 | 4     |
| FILE\_ATTRIBUTE\_DIRECTORY  | 0x00000010 | 16    |
| Datei \_ Attribut \_ temporär  | 0x00000100 | 256   |
| FILE\_ATTRIBUTE\_COMPRESSED | 0x00000800 | 2048  |
| FILE\_ATTRIBUTE\_OFFLINE    | 0x00001000 | 4096  |



 

Gibt – 1 zurück, wenn die Datei oder der Ordner nicht vorhanden oder nicht zugänglich ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| Header<br/>  | <dl> <dt>Windows. Storage. h</dt> </dl>                                                                                                                                                            |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




