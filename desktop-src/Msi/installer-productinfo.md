---
description: Die ProductInfo-Eigenschaft ist eine schreibgeschützte Eigenschaft, die den Wert des angegebenen Attributs für ein installiertes oder veröffentlichtes Produkt zurückgibt.
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: Installer. ProductInfo-Eigenschaft ("oemupgex. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 03ad741dd1c92fe68caccc4582738e54032750e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354803"
---
# <a name="installerproductinfo-property"></a>Installer. ProductInfo-Eigenschaft

Die **productinfo** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die den Wert des angegebenen Attributs für ein installiertes oder veröffentlichtes Produkt zurückgibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Die **productinfo** -Eigenschaft ("localpackage") gibt nicht notwendigerweise einen Pfad zum zwischengespeicherten Paket zurück. Wartungsmodus-Installationen sollten nicht über das localpackage aufgerufen werden. Das zwischengespeicherte Paket ist nur für die interne Verwendung vorgesehen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.<br/> |
| Header<br/>  | <dl> <dt>"Oemupgex. h"</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msigetproductinfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**Msigetuserinfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




