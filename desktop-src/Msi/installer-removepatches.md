---
description: Mit der removepatches-Methode werden ein oder mehrere Patches zu Produkten entfernt, die zum Empfangen des Patches berechtigt sind. Die removepatches-Methode ruft msiremovepatches auf.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Installer. removepatches-Methode
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
ms.openlocfilehash: 2130ae2958f03eb16b5145e5eb61e42f869ad775
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355926"
---
# <a name="installerremovepatches-method"></a>Installer. removepatches-Methode

Mit der **removepatches** -Methode werden ein oder mehrere Patches zu Produkten entfernt, die zum Empfangen des Patches berechtigt sind. Die **removepatches** -Methode ruft [**msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)auf.

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

*Patchliste* 
</dt> <dd>

Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der zu entfernenden Patches enthält. Jeder Patch kann entweder durch den vollständigen Pfad zum Patchpaket oder durch die Patch-GUID dargestellt werden. Dieser Parameter ist erforderlich.

</dd> <dt>

*ProductCode* 
</dt> <dd>

Eine Zeichenfolge mit der GUID des Produkts, von dem die Patches entfernt werden sollen. Dieser Parameter ist erforderlich.

</dd> <dt>

*Uninstalltype* 
</dt> <dd>

Ein ganzzahliger Wert, der den Typ der Patchentfernung angibt. Dieser Parameter muss " **msiinstalltypesinglabstance**" lauten.

</dd> <dt>

*Eigenschaftsliste* 
</dt> <dd>

Eine Zeichenfolge, die die einzuschließ-Wert Paare der Eigenschaft = Wert angibt. Dieser Parameter ist optional.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Unter [Deinstallieren von Patches](uninstalling-patches.md) finden Sie ein Beispiel, das veranschaulicht, wie eine Anwendung einen Patch von allen Produkten entfernen kann, die für den Benutzer verfügbar sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**Msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Patches werden deinstalliert.](uninstalling-patches.md)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




