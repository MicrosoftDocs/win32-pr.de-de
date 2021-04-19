---
description: Die productelevated-Eigenschaft des Installer-Objekts gibt true zurück, wenn das Produkt verwaltet wird, oder false, wenn das Produkt nicht verwaltet wird.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Installer::P roductelevated-Eigenschaft
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
ms.openlocfilehash: 22591c20cbabfda2eb052e4746e87739b9681804
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367818"
---
# <a name="installerproductelevated-property"></a>Installer::P roductelevated-Eigenschaft

Die **productelevated** -Eigenschaft des [**Installer**](installer-object.md) -Objekts gibt true zurück, wenn das Produkt verwaltet wird, oder false, wenn das Produkt nicht verwaltet wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a>Eigenschaftswert

Die vollständige Produktcode-GUID des Produkts. Dieser Parameter ist erforderlich.

## <a name="remarks"></a>Bemerkungen

Die **productelevated** -Eigenschaft verwendet die [**msiisproductelevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) -Funktion. Bei der Rückgabe der Eigenschaft wird die [alwaysinstallerhöhten](alwaysinstallelevated.md) -Richtlinie nicht berücksichtigt.

## <a name="examples"></a>Beispiele

Im folgenden Beispielskript wird die Verwendung der **productelevated** -Eigenschaft veranschaulicht.


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
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 4,5 unter Windows Server 2003 und Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Installationsprogramm**](installer-object.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




