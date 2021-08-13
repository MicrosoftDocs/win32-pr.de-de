---
description: Das Product-Objekt stellt eine eindeutige Instanz eines Produkts dar, das entweder angekündigt, installiert oder unbekannt ist. Das Objekt kann mit der Product-Eigenschaft als &\# 0034 instanziiert werden. WindowsInstaller.Installer.Product(ProductCode, UserSid, Context)&\# 0034;.
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Product-Objekt
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
# <a name="product-object"></a>Product-Objekt

Das **Product-Objekt** stellt eine eindeutige Instanz eines Produkts dar, das entweder angekündigt, installiert oder unbekannt ist.

Das -Objekt kann mit der **Product-Eigenschaft** als "WindowsInstaller.Installer.Product(*ProductCode*, *UserSid*, *Context*)" instanziiert werden. *UserSid* muss für den Kontext pro Computer NULL sein. *UserSid* kann NULL für den angegebenen aktuellen Benutzer sein, wenn der Kontext nicht pro Computer ist. Die Parameter *ProductCode* und *Context* sind erforderlich.

## <a name="members"></a>Member

Das **Product-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Product-Objekt** verfügt über diese Methoden.



| Methode                                                                 | Beschreibung                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)       | Fügen Sie der Gruppe der registrierten Datenträger einen Datenträger hinzu.<br/>                                                              |
| [**SourceListAddSource**](product-sourcelistaddsource.md)             | Fügen Sie der Quellliste ein Netzwerk oder eine URL-Quelle hinzu.<br/>                                                         |
| [**SourceListClearAll**](product-sourcelistclearall.md)               | Löscht die vollständige Quellliste des angegebenen Quellentyps.<br/>                                       |
| [**SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)   | Entfernen Sie einen Datenträger aus dem Satz der registrierten Datenträger aus der Quellliste.<br/>                                    |
| [**SourceListClearSource**](product-sourcelistclearsource.md)         | Entfernen Sie ein Netzwerk oder eine URL-Quelle aus der Quellliste.<br/>                                                    |
| [**SourceListForceResolution**](product-sourcelistforceresolution.md) | Löscht die zuletzt verwendete Quelle. Dies erzwingt eine Quelllistenauflösung, wenn die Quelle das nächste Mal benötigt wird.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **Product-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Beschreibung                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**ComponentState**](product-componentstate.md)<br/>   | Der Zustand einer angegebenen Komponente für diese Produktinstanz. <br/>                   |
| [**Kontext**](product-context.md)<br/>                 | Der Kontext dieser Produktinstanz als MSIINSTALLCONTEXT-Wert. <br/>                 |
| [**FeatureState**](product-featurestate.md)<br/>       | Der Status eines angegebenen Features für diese Produktinstanz. <br/>                     |
| [**InstallProperty**](product-installproperty.md)<br/> | Der Wert einer angegebenen Eigenschaft. <br/>                                              |
| [**MediaDisks**](product-mediadisks.md)<br/>           | Listet alle Mediendatenträger für diese Produktinstanz auf.<br/>                        |
| [**ProductCode**](product-productcode.md)<br/>         | Gibt den Produktcode zurück. <br/>                                                       |
| [**SourceListInfo**](product-sourcelistinfo.md)<br/>   | Abrufen und Festlegen der Quellinformationseigenschaften. Dies ist eine Lese- oder Schreibeigenschaft.<br/> |
| [**Quellen**](product-sources.md)<br/>                 | Listet alle Quellen für diese Produktinstanz auf.<br/>                            |
| [**State**](product-state.md)<br/>                     | Installationsstatus des Produkts.<br/>                                               |
| [**UserSid**](product-usersid.md)<br/>                 | Gibt die Benutzer-SID zurück, unter der dieses Konto für diese Produktinstanz verfügbar ist.<br/>    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct ist als 000C10A0-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Windows Beispiele für Skripterstellung für Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




