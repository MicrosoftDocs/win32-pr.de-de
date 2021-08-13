---
description: Die ApplyMultiplePatches-Methode wendet ein oder mehrere Patches auf Produkte an, die für den Patch berechtigt sind. Die -Methode legt die PATCH-Eigenschaft fest.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Installer.ApplyMultiplePatches-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a2b1c469ca623b0c09ea2899de1867cc10c8d8cda9363994973d08ecc20ed7f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633207"
---
# <a name="installerapplymultiplepatches-method"></a>Installer.ApplyMultiplePatches-Methode

Die **ApplyMultiplePatches-Methode** wendet ein oder mehrere Patches auf Produkte an, die für den Patch berechtigt sind. Die -Methode legt die [**PATCH-Eigenschaft**](patch.md) fest.

## <a name="syntax"></a>Syntax


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PatchPackagesList* 
</dt> <dd>

Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der Pfade zum Patchen von Dateien enthält. Beispiel: ""c: \\ sus \\ download cache Office \\ \\ \\ sp1.msp; c: \\ sus \\ download cache \\ Office \\ \\ QFE1.msp;c: \\ sus download cache Office \\ \\ \\ \\ SELECTEn.msp""

</dd> <dt>

*Produkt* 
</dt> <dd>

Dieser Parameter stellt den [**ProductCode**](productcode.md) des Produkts bereit, das gepatcht wird. Dieser Parameter ist optional. Wenn dieser Parameter NULL ist, werden die Patches auf alle Produkte angewendet, die für den Empfang dieser Patches berechtigt sind.

</dd> <dt>

*szPropertiesList* 
</dt> <dd>

Eine auf NULL endende Zeichenfolge, die Befehlszeileneigenschafteneinstellungen angibt. Dieser Parameter ist optional. Weitere Informationen finden Sie unter [Informationen zu Eigenschaften](about-properties.md) und Festlegen öffentlicher [Eigenschaftswerte in der Befehlszeile.](setting-public-property-values-on-the-command-line.md) Diese Eigenschaften werden von allen Zielprodukten gemeinsam genutzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 3.0 oder höher auf Windows Server 2003 oder Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Informationen zu Eigenschaften](about-properties.md)
</dt> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**Patch**](patch.md)
</dt> <dt>

[Festlegen öffentlicher Eigenschaftswerte in der Befehlszeile](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




