---
description: Die Environment-Eigenschaft des Installer-Objekts ist eine Lese-/Schreibeigenschaft, die der Zeichen folgen Wert für eine Umgebungsvariable des aktuellen Prozesses ist.
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: Installer. Environment (Eigenschaft)
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
ms.openlocfilehash: 3983eceecd8bc709bea4a094c61c9886c73def3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350776"
---
# <a name="installerenvironment-property"></a>Installer. Environment (Eigenschaft)

Die **Environment** -Eigenschaft des [**Installer**](installer-object.md) -Objekts ist eine Lese-/Schreibeigenschaft, die der Zeichen folgen Wert für eine Umgebungsvariable des aktuellen Prozesses ist.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

Der Name der Umgebungsvariablen, die gelesen oder geschrieben werden soll. Dabei wird die Groß-/Kleinschreibung beachtet.

## <a name="remarks"></a>Bemerkungen

Das Festlegen einer Umgebungsvariablen mit der- **Umgebungs** Eigenschaft wirkt sich nur auf die aktive Sitzung aus. Wenn Sie persistente Änderungen an einer Umgebungsvariablen vornehmen möchten, verwenden Sie die [Umgebungs Tabelle](environment-table.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




