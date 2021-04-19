---
description: Gibt ein RecordList-Objekt zurück, das Produkte auflistet, die eine angegebene installierte Komponente verwenden.
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: Installer. clientsex (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClientsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5a609ab0ba6edc5b0e3e9bbd26bc3539858ebdee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355942"
---
# <a name="installerclientsex-property"></a>Installer. clientsex (Eigenschaft)

Diese Eigenschaft gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das Produkte auflistet, die eine angegebene installierte Komponente verwenden. Diese Eigenschaft ruft [**msienumschlag clientsex**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)auf.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Diese Eigenschaft ist ab Windows Installer 5,0 verfügbar.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ClientsEx
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

[**Msienumschlag clientsex**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




