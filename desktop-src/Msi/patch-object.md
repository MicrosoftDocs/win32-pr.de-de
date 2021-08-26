---
description: Das Patch-Objekt stellt eine eindeutige Instanz eines Patches dar, das registriert oder angewendet wurde. Das -Objekt kann mit der Patch-Eigenschaft wie &\# 0034 instanziiert werden. WindowsInstaller.Installer.Patch(PatchCode, ProductCode, UserSid, Context)&\# 0034;.
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
ms.openlocfilehash: e9e337af735a39312cb5aa740283cb8b4d8b508be33f28c302788a1207f89472
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074840"
---
# <a name="patch-object"></a>Patch-Objekt

Das **Patch-Objekt** stellt eine eindeutige Instanz eines Patches dar, das registriert oder angewendet wurde.

Das -Objekt kann mit der **Patch-Eigenschaft** als "WindowsInstaller.Installer.Patch(*PatchCode*, *ProductCode*, *UserSid*, *Context*)" instanziiert werden. Bei einem Computerkontext muss der *UserSid-Parameter* eine leere Zeichenfolge sein. ProductCode *kann* auf eine leere Zeichenfolge für Patches festgelegt werden, die nur registriert und noch nicht auf ein Produkt angewendet wurden. Der *ProductCode kann* auf eine leere Zeichenfolge festgelegt werden, wenn nur die Quelllisteninformationen eines Patches gelesen oder aktualisiert werden.

## <a name="members"></a>Member

Das **Patch-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Patch-Objekt** verfügt über diese Methoden.



| Methode                                                               | BESCHREIBUNG                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)       | Fügen Sie dem Satz registrierter Datenträger einen Datenträger hinzu.<br/>                                                                                   |
| [**SourceListAddSource**](patch-sourcelistaddsource.md)             | Fügen Sie der Quellliste eine Netzwerk- oder URL-Quelle hinzu. <br/>                                                                             |
| [**SourceListClearAll**](patch-sourcelistclearall.md)               | Löschen der vollständigen Quellliste des angegebenen Quellentyps.<br/>                                                            |
| [**SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)   | Entfernen Sie einen Datenträger aus dem Satz registrierter Datenträger aus der Quellliste. <br/>                                                        |
| [**SourceListClearSource**](patch-sourcelistclearsource.md)         | Entfernen Sie eine Netzwerk- oder URL-Quelle aus der Quellliste.<br/>                                                                         |
| [**SourceListForceResolution**](patch-sourcelistforceresolution.md) | Entfernt die zuletzt verwendete Quelle aus der Quellliste. Dies erzwingt eine Quelllistenauflösung, wenn die Quelle das nächste Mal benötigt wird.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **Patch-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                  | BESCHREIBUNG                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Kontext**](patch-context.md)<br/>               | Der Kontext dieser Patchinstanz ist ein MSIINSTALLCONTEXT-Wert.<br/>                                   |
| [**MediaDisks**](patch-mediadisks.md)<br/>         | Enumeriert alle Mediendatenträger für diese Patchinstanz.<br/>                                         |
| [**PatchCode**](patch-patchcode.md)<br/>           | Gibt den Patchcode zurück.<br/>                                                                         |
| [**PatchProperty**](patch-patchproperty.md)<br/>   | Ruft Eigenschafteninformationen zu einem bestimmten Patch ab, der auf eine bestimmte Instanz des Produkts angewendet wird.<br/> |
| [**ProductCode**](patch-productcode.md)<br/>       | Gibt den Produktcode zurück.<br/>                                                                       |
| [**SourceListInfo**](patch-sourcelistinfo.md)<br/> | Ruft die Quellinformationseigenschaften ab und legt sie fest. Dies ist eine Lese- oder Schreibeigenschaft.<br/>              |
| [**Quellen**](patch-sources.md)<br/>               | Enumeriert alle Quellen für diese Patchinstanz.<br/>                                             |
| [**State**](patch-state.md)<br/>                   | Installationsstatus des Patches.<br/>                                                                |
| [**UserSid**](patch-usersid.md)<br/>               | Gibt die Benutzer-SID unter dem Konto zurück, unter dem diese Patchinstanz verfügbar ist.<br/>                       |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch ist als \_ 000C10A1-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Windows Skriptbeispiele für Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




