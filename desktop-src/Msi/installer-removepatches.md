---
description: Die RemovePatches-Methode entfernt ein oder mehrere Patches für Produkte, die zum Empfangen des Patches berechtigt sind. Die RemovePatches-Methode ruft MsiRemovePatches auf.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Installer.RemovePatches-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bfa316b4ff01f6e5667b3fb2c5fce2333c4b4aaf34dc5a1dbb37feb61d1a9ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894030"
---
# <a name="installerremovepatches-method"></a>Installer.RemovePatches-Methode

Die **RemovePatches-Methode** entfernt ein oder mehrere Patches für Produkte, die zum Empfangen des Patches berechtigt sind. Die **RemovePatches-Methode** ruft [**MsiRemovePatches auf.**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)

## <a name="syntax"></a>Syntax


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PatchList* 
</dt> <dd>

Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der zu entfernenden Patches enthält. Jeder Patch kann entweder durch den vollständigen Pfad zum Patchpaket oder durch die Patch-GUID dargestellt werden. Dieser Parameter ist erforderlich.

</dd> <dt>

*ProductCode* 
</dt> <dd>

Eine Zeichenfolge mit der GUID des Produkts, aus dem die Patches entfernt werden sollen. Dieser Parameter ist erforderlich.

</dd> <dt>

*UninstallType* 
</dt> <dd>

Ein ganzzahliger Wert, der den Typ der Patchentfernung angibt. Dieser Parameter muss **msiInstallTypeSingleInstance sein.**

</dd> <dt>

*Eigenschaftsliste* 
</dt> <dd>

Eine Zeichenfolge, die die property=Value-Paare angibt, die enthalten sein müssen. Dieser Parameter ist optional.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Unter [Deinstallieren von Patches finden](uninstalling-patches.md) Sie ein Beispiel, das veranschaulicht, wie eine Anwendung einen Patch von allen Produkten entfernen kann, die für den Benutzer verfügbar sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003 oder Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Deinstallieren von Patches](uninstalling-patches.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




