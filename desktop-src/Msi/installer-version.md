---
description: Die Version-Eigenschaft des Installer-Objekts ist eine schreibgeschützte Eigenschaft, die die Zeichenfolgendarstellung der aktuellen Version von Windows Installer ist. Die Zeichenfolge wird im folgenden Format zurückgegeben.
ms.assetid: 9af262f0-b573-471d-aac6-6a72e8cb5314
title: Installer.Version-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Version
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3d2aeb845647317751eba53caae1609f8d3d66f9f7d373aa7faa24e3b8cdfb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119295547"
---
# <a name="installerversion-property"></a>Installer.Version-Eigenschaft

Die **Version-Eigenschaft** des [**Installer-Objekts**](installer-object.md) ist eine schreibgeschützte Eigenschaft, die die Zeichenfolgendarstellung der aktuellen Version von Windows Installer ist. Die Zeichenfolge wird im folgenden Format zurückgegeben.

*Haupt-*. *nebenversion*. *build*. *aktualisieren*

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.Version
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



 

 




