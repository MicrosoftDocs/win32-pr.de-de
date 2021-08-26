---
description: Die ProductElevated-Eigenschaft des Installer-Objekts gibt True zurück, wenn das Produkt verwaltet wird, oder False, wenn das Produkt nicht verwaltet wird.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Installer::P ro enthaltenElevated-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 515964481c62e4588f3d9b75d168bffd2876cb22ce526e8ec0eaa41e226c110e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129390"
---
# <a name="installerproductelevated-property"></a>Installer::P ro enthaltenElevated-Eigenschaft

Die **ProductElevated-Eigenschaft** des [**Installer-Objekts**](installer-object.md) gibt True zurück, wenn das Produkt verwaltet wird, oder False, wenn das Produkt nicht verwaltet wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a>Eigenschaftswert

Die vollständige Produktcode-GUID des Produkts. Dieser Parameter ist erforderlich.

## <a name="remarks"></a>Hinweise

Die **ProductElevated-Eigenschaft** verwendet die [**MsiIsProductElevated-Funktion.**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) Bei der Rückgabe der -Eigenschaft wird die [AlwaysInstallElevated-Richtlinie nicht](alwaysinstallelevated.md) berücksichtigt.

## <a name="examples"></a>Beispiele

Das folgende Beispielskript veranschaulicht die Verwendung der **ProductElevated-Eigenschaft.**


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 4.5 auf Windows Server 2003 und Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Installer**](installer-object.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 3.1 und früheren Versionen](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




