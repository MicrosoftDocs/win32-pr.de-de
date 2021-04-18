---
description: Die applymultiplepatches-Methode wendet ein oder mehrere Patches auf Produkte an, die zum Empfangen des Patches berechtigt sind. Mit der-Methode wird die Patch-Eigenschaft festgelegt.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Installer. applymultiplepatches-Methode
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
ms.openlocfilehash: d96d96157f7b1d81617be6980804fb54a6e6659f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357685"
---
# <a name="installerapplymultiplepatches-method"></a>Installer. applymultiplepatches-Methode

Die **applymultiplepatches** -Methode wendet ein oder mehrere Patches auf Produkte an, die zum Empfangen des Patches berechtigt sind. Mit der-Methode wird die [**Patch**](patch.md) -Eigenschaft festgelegt.

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

*Patchpackageslist* 
</dt> <dd>

Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der Pfade zu Patchdateien enthält. Beispiel: "" c: \\ SUS \\ Download \\ Cache \\ Office \\ SP1. msp; c: \\ SUS \\ Download \\ Cache \\ Office \\ QFE1. msp; c: \\ SUS \\ Download \\ Cache \\ Office \\ qfen. msp ""

</dd> <dt>

*Produkt* 
</dt> <dd>

Dieser Parameter stellt den [**ProductCode**](productcode.md) des Produkts bereit, das gepatcht wird. Dieser Parameter ist optional. Wenn dieser Parameter NULL ist, werden die Patches auf alle Produkte angewendet, die für den Empfang dieser Patches berechtigt sind.

</dd> <dt>

*szpropertieslist* 
</dt> <dd>

Eine auf NULL endenden Zeichenfolge, die Befehlszeilen-Eigenschafts Einstellungen angibt. Dieser Parameter ist optional. Weitere Informationen finden Sie unter [Informationen zu Eigenschaften](about-properties.md) und [festlegen öffentlicher Eigenschaftswerte in der Befehlszeile](setting-public-property-values-on-the-command-line.md). Diese Eigenschaften werden von allen Ziel Produkten gemeinsam genutzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Informationen zu Eigenschaften](about-properties.md)
</dt> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**Patch**](patch.md)
</dt> <dt>

[Festlegen von Werten für öffentliche Eigenschaften in der Befehlszeile](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[**Msiapplymultiplepatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




