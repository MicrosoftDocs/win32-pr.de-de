---
description: Die Environment-Eigenschaft des Installer-Objekts ist eine Lese-/Schreibeigenschaft, die der Zeichenfolgenwert für eine Umgebungsvariable des aktuellen Prozesses ist.
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: Installer.Environment (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Environment
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f24237da6c140ef0d38ff17591bf214698cfa6731bd4e8d3cfcaa613b335404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631686"
---
# <a name="installerenvironment-property"></a>Installer.Environment (Eigenschaft)

Die **Environment-Eigenschaft** des [**Installer-Objekts**](installer-object.md) ist eine Lese-/Schreibeigenschaft, die der Zeichenfolgenwert für eine Umgebungsvariable des aktuellen Prozesses ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

Der Name der Zu lesenden oder zu schreibenden Umgebungsvariablen. Dabei wird die Groß-/Kleinschreibung nicht beachtet.

## <a name="remarks"></a>Hinweise

Das Festlegen einer Umgebungsvariablen **mit der Environment-Eigenschaft** wirkt sich nur auf die aktive Sitzung aus. Verwenden Sie die Umgebungstabelle , um persistente Änderungen an einer [Umgebungsvariablen vorzunehmen.](environment-table.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



 

 




