---
description: Das Product-Objekt stellt eine eindeutige Instanz eines Produkts dar, das entweder angekündigt, installiert oder unbekannt ist. Das Objekt kann mit der Product-Eigenschaft wie &\# 0034 instanziiert werden. WindowsInstaller.Installer.Product(ProductCode, UserSid, Context)&\# 0034;.
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Produktobjekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ff05a2f89244da09caa6cd3b26fc4b5d9cdbec95c0fcc3098fddf0c39dc68519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627673"
---
# <a name="product-object"></a>Produktobjekt

Das **Product-Objekt** stellt eine eindeutige Instanz eines Produkts dar, das entweder angekündigt, installiert oder unbekannt ist.

Das Objekt kann mit der **Product-Eigenschaft** als "WindowsInstaller.Installer.Product(*ProductCode,* *UserSid*, *Context )" instanziiert* werden. *UserSid muss* für den Kontext pro Computer NULL sein. *UserSid kann* null für den angegebenen aktuellen Benutzer sein, wenn der Kontext nicht pro Computer ist. *Die Parameter ProductCode* *und Context* sind erforderlich.

## <a name="members"></a>Member

Das **Product-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Product-Objekt** verfügt über diese Methoden.



| Methode                                                                 | Beschreibung                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)       | Fügen Sie dem Satz registrierter Datenträger einen Datenträger hinzu.<br/>                                                              |
| [**SourceListAddSource**](product-sourcelistaddsource.md)             | Fügen Sie der Quellliste eine Netzwerk- oder URL-Quelle hinzu.<br/>                                                         |
| [**SourceListClearAll**](product-sourcelistclearall.md)               | Löschen der vollständigen Quellliste des angegebenen Quellentyps.<br/>                                       |
| [**SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)   | Entfernen Sie einen Datenträger aus dem Satz registrierter Datenträger aus der Quellliste.<br/>                                    |
| [**SourceListClearSource**](product-sourcelistclearsource.md)         | Entfernen Sie eine Netzwerk- oder URL-Quelle aus der Quellliste.<br/>                                                    |
| [**SourceListForceResolution**](product-sourcelistforceresolution.md) | Löschen der zuletzt verwendeten Quelle. Dies erzwingt eine Quelllistenauflösung, wenn die Quelle das nächste Mal benötigt wird.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **Product-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Beschreibung                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**ComponentState**](product-componentstate.md)<br/>   | Der Zustand einer angegebenen Komponente für diese Produktinstanz. <br/>                   |
| [**Kontext**](product-context.md)<br/>                 | Kontext dieser Produktinstanz als MSIINSTALLCONTEXT-Wert. <br/>                 |
| [**FeatureState**](product-featurestate.md)<br/>       | Der Status eines angegebenen Features für diese Produktinstanz. <br/>                     |
| [**InstallProperty**](product-installproperty.md)<br/> | Der Wert einer angegebenen Eigenschaft. <br/>                                              |
| [**MediaDisks**](product-mediadisks.md)<br/>           | Enumeriert alle Mediendatenträger für diese Produktinstanz.<br/>                        |
| [**ProductCode**](product-productcode.md)<br/>         | Gibt den Produktcode zurück. <br/>                                                       |
| [**SourceListInfo**](product-sourcelistinfo.md)<br/>   | Hier können Sie die Quellinformationseigenschaften erhalten und festlegen. Dies ist eine Lese- oder Schreibeigenschaft.<br/> |
| [**Quellen**](product-sources.md)<br/>                 | Enumeriert alle Quellen für diese Produktinstanz.<br/>                            |
| [**State**](product-state.md)<br/>                     | Installationsstatus des Produkts.<br/>                                               |
| [**UserSid**](product-usersid.md)<br/>                 | Gibt die Benutzer-SID zurück, unter der diese Produktinstanz verfügbar ist.<br/>    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct ist als \_ 000C10A0-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Windows Skriptbeispiele für Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




