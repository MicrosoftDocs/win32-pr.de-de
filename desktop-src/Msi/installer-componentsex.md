---
description: Gibt ein RecordList-Objekt zurück, das installierte Komponenten auflistet.
ms.assetid: a91656de-2ebc-45b5-86f8-b13f35c6a762
title: Installer.ComponentsEx (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1805780c7d21018ec51273b00df88493e25a38dd4525428ba605f8fa9934ceaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632318"
---
# <a name="installercomponentsex-property"></a>Installer.ComponentsEx (Eigenschaft)

Diese Eigenschaft gibt ein [**RecordList-Objekt**](recordlist-object.md) zurück, das installierte Komponenten auflistet. Diese Eigenschaft ruft [**MsiEnumComponentsEx auf.**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt. Diese Eigenschaft ist ab Windows Installer 5.0 verfügbar.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ComponentsEx
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
</dt> </dl>

 

 




