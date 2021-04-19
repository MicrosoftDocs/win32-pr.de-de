---
description: Die productinfofromscript-Eigenschaft des Installer-Objekts gibt den Wert des angegebenen Attributs zurück, das in einem Ankündigungs Skript gespeichert ist.
ms.assetid: 92aa479b-2b4c-482c-a186-a290461bc6d8
title: Installer::P der Eigenschaft "roductinfofromscript"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfoFromScript
- Installer.put_ProductInfoFromScript
- Installer.ProductInfoFromScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a4c8e29adb93f68228008770a95ad9fb9185e966
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372483"
---
# <a name="installerproductinfofromscript-property"></a>Installer::P der Eigenschaft "roductinfofromscript"

Die **productinfofromscript** -Eigenschaft des [**Installer**](installer-object.md) -Objekts gibt den Wert des angegebenen Attributs zurück, das in einem Ankündigungs Skript gespeichert ist.

Diese Eigenschaft ist lesegeschützt.

## <a name="syntax"></a>Syntax


```JScript
Installer.ProductInfoFromScript = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="error-codes"></a>Fehlercodes

Eine Zeichenfolge oder ein ganzzahliger Wert, abhängig vom angeforderten Attribut.

## <a name="remarks"></a>Bemerkungen

Die **productinfofromscript** -Eigenschaft verwendet die [**msigetproductinfofromscript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) -Funktion.

## <a name="examples"></a>Beispiele

Das folgende Beispielskript veranschaulicht die Verwendung der **productinfofromscript** -Eigenschaft.


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Create an advertise script for Orca
'

installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scratch\orca.aas"

' 
' Output ProductName Information From Script
'

MsgBox  installer.ProductInfoFromScript("c:\scratch\orca.aas", 3)
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

 

 




