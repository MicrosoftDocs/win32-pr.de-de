---
description: Gibt ein RecordList-Objekt zurück, das den vollständigen Pfad einer angegebenen installierten Komponente angibt.
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: Installer.ComponentPathEx-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 720b10c75fcdf4a6b72f22a72d3b0860fc6089403385b0a951127f56286b6953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632615"
---
# <a name="installercomponentpathex-property"></a>Installer.ComponentPathEx-Eigenschaft

Diese Eigenschaft gibt ein [**RecordList-Objekt**](recordlist-object.md) zurück, das den vollständigen Pfad einer angegebenen installierten Komponente angibt. Diese Eigenschaft ruft [**MsiGetComponentPathEx auf.**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Wird nicht unterstützt. Diese Eigenschaft ist ab Windows Installer 5.0 verfügbar.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




