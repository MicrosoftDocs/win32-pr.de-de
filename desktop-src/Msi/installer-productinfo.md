---
description: Die ProductInfo-Eigenschaft ist eine schreibgeschützte Eigenschaft, die den Wert des angegebenen Attributs für ein installiertes oder veröffentlichtes Produkt zurückgibt.
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: Installer.ProductInfo-Eigenschaft (Oemupgex.h)
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
ms.openlocfilehash: 5d04ad49fd8c1cf017131b5ded6be088e6436731b6bd97dd437060d09988d3aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745290"
---
# <a name="installerproductinfo-property"></a>Installer.ProductInfo-Eigenschaft

Die **ProductInfo-Eigenschaft** ist eine schreibgeschützte Eigenschaft, die den Wert des angegebenen Attributs für ein installiertes oder veröffentlichtes Produkt zurückgibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Die **ProductInfo-Eigenschaft** ("LocalPackage") gibt nicht unbedingt einen Pfad zum zwischengespeicherten Paket zurück. Installationen im Wartungsmodus sollten nicht über localPackage aufgerufen werden. Das zwischengespeicherte Paket ist nur für interne Verwendungszwecke vorgesehen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 3.0 oder höher auf Windows Server 2003 oder Windows XP.<br/> |
| Header<br/>  | <dl> <dt>Oemupgex.h</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




