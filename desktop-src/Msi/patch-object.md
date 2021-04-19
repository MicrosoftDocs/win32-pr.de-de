---
description: Das Patch-Objekt stellt eine eindeutige Instanz eines Patches dar, die registriert oder angewendet wurde. Das Objekt kann mit der Patch-Eigenschaft wie &0034 instanziiert werden \# . WindowsInstaller. Installer. Patch (Patchcode, ProductCode, UserSID, context) &\# 0034;.
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Patch-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f6fa55d6ced2afdc53ef8050732f5dee5d6c1f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367561"
---
# <a name="patch-object"></a>Patch-Objekt

Das **Patch** -Objekt stellt eine eindeutige Instanz eines Patches dar, die registriert oder angewendet wurde.

Das Objekt kann mit der **Patch** -Eigenschaft als "WindowsInstaller. Installer. Patch (*Patchcode*, *ProductCode*, *UserSID*, *context*)" instanziiert werden. Bei einem Computer Kontext muss der *UserSID* -Parameter eine leere Zeichenfolge sein. *ProductCode* kann auf eine leere Zeichenfolge für Patches festgelegt werden, die nur registriert sind und noch nicht auf ein Produkt angewendet wurden. *ProductCode* kann auf eine leere Zeichenfolge festgelegt werden, wenn nur die Quell Listen Informationen eines Patches gelesen oder aktualisiert werden.

## <a name="members"></a>Member

Das **Patch** -Objekt verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Patch** -Objekt verfügt über diese Methoden.



| Methode                                                               | BESCHREIBUNG                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Sourcelistaddmediadisk**](patch-sourcelistaddmediadisk.md)       | Fügen Sie dem Satz registrierter Datenträger einen Datenträger hinzu.<br/>                                                                                   |
| [**Sourcelistaddsource**](patch-sourcelistaddsource.md)             | Fügen Sie der Quell Liste eine Netzwerk-oder URL-Quelle hinzu. <br/>                                                                             |
| [**Sourcelistclearall**](patch-sourcelistclearall.md)               | Löscht die gesamte Quell Liste des angegebenen Quellen Typs.<br/>                                                            |
| [**Sourcelistclearmediadisk**](patch-sourcelistclearmediadisk.md)   | Entfernen Sie einen Datenträger aus der Gruppe der registrierten Datenträger aus der Quell Liste. <br/>                                                        |
| [**Sourcelistclearsource**](patch-sourcelistclearsource.md)         | Entfernen Sie eine Netzwerk-oder URL-Quelle aus der Quell Liste.<br/>                                                                         |
| [**Sourcelistforceresolution**](patch-sourcelistforceresolution.md) | Löscht die zuletzt verwendete Quelle aus der Quell Liste. Dadurch wird eine Quell Listen Auflösung erzwungen, wenn die Quelle das nächste Mal benötigt wird.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **patchobjekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                  | BESCHREIBUNG                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Kontext**](patch-context.md)<br/>               | Der Kontext dieser patchinstanz ist ein msiinstallcontext-Wert.<br/>                                   |
| [**Mediadisks**](patch-mediadisks.md)<br/>         | Listet alle Medien Datenträger für diese patchinstanz auf.<br/>                                         |
| [**Patchcode**](patch-patchcode.md)<br/>           | Gibt den Patchcode zurück.<br/>                                                                         |
| [**Patcheigenschaft**](patch-patchproperty.md)<br/>   | Ruft Eigenschaften Informationen zu einem bestimmten Patch ab, der auf eine bestimmte Instanz des Produkts angewendet wird.<br/> |
| [**ProductCode**](patch-productcode.md)<br/>       | Gibt den Produktcode zurück.<br/>                                                                       |
| [**Sourcelistinfo**](patch-sourcelistinfo.md)<br/> | Ruft die Quell Informations Eigenschaften ab und legt Sie fest. Dies ist eine Lese-oder Schreib Eigenschaft.<br/>              |
| [**Sources**](patch-sources.md)<br/>               | Listet alle Quellen für diese patchinstanz auf.<br/>                                             |
| [**State**](patch-state.md)<br/>                   | Der Installationsstatus des Patches.<br/>                                                                |
| [**UserSID**](patch-usersid.md)<br/>               | Gibt die Benutzer-SID unter dem Konto zurück, auf dem diese patchinstanz verfügbar ist.<br/>                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




