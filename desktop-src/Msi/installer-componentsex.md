---
description: Gibt ein RecordList-Objekt zurück, das installierte Komponenten auflistet.
ms.assetid: a91656de-2ebc-45b5-86f8-b13f35c6a762
title: Installer. componentsex (Eigenschaft)
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
ms.openlocfilehash: 1a48261a924280999d2b8329d635d4115de35753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372623"
---
# <a name="installercomponentsex-property"></a>Installer. componentsex (Eigenschaft)

Diese Eigenschaft gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das installierte Komponenten auflistet. Diese Eigenschaft ruft [**msienumschlag componentsex**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)auf.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Diese Eigenschaft ist ab Windows Installer 5,0 verfügbar.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ComponentsEx
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

[**Msienumschlag**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
</dt> </dl>

 

 




