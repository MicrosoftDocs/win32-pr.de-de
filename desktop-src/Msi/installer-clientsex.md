---
description: Gibt ein RecordList-Objekt zurück, das Produkte auflistet, die eine angegebene installierte Komponente verwenden.
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: Installer.ClientsEx (Eigenschaft)
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
ms.openlocfilehash: 54ecc8c0d76ae5105aec07a85adb18d93a8e7a9b75162f8124bb32fdd7f64597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632927"
---
# <a name="installerclientsex-property"></a>Installer.ClientsEx (Eigenschaft)

Diese Eigenschaft gibt ein [**RecordList-Objekt**](recordlist-object.md) zurück, das Produkte auflistet, die eine angegebene installierte Komponente verwenden. Diese Eigenschaft ruft [**MsiEnumClientsEx auf.**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt. Diese Eigenschaft ist ab Windows Installer 5.0 verfügbar.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ClientsEx
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

[**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




