---
description: Gibt ein RecordList-Objekt zurück, das den vollständigen Pfad einer angegebenen installierten Komponente enthält.
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: Installer. componentpathex-Eigenschaft
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
ms.openlocfilehash: b7bf98dd8e7a81a0dd261f22a565bec8298a86a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368467"
---
# <a name="installercomponentpathex-property"></a>Installer. componentpathex-Eigenschaft

Diese Eigenschaft gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das den vollständigen Pfad einer angegebenen installierten Komponente enthält. Diese Eigenschaft ruft [**msigetcomponentpathex**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)auf.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Diese Eigenschaft ist ab Windows Installer 5,0 verfügbar.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msigetcomponentpathex**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




