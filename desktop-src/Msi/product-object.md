---
description: Das Product-Objekt stellt eine eindeutige Instanz eines Produkts dar, das entweder angekündigt, installiert oder unbekannt ist. Das Objekt kann mit der Product-Eigenschaft wie &0034 instanziiert werden \# . WindowsInstaller. Installer. Product (ProductCode, UserSID, context) &\# 0034;.
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
ms.openlocfilehash: f8e9071f26da944c2c5ea206b2f70582d731ef59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357615"
---
# <a name="product-object"></a>Product-Objekt

Das **Product** -Objekt stellt eine eindeutige Instanz eines Produkts dar, das entweder angekündigt, installiert oder unbekannt ist.

Das Objekt kann mit der **Product** -Eigenschaft als "WindowsInstaller. Installer. Product (*ProductCode*, *UserSID*, *context*)" instanziiert werden. *UserSID* muss für computerspezifischen Kontext null sein. *UserSID* kann NULL für den angegebenen aktuellen Benutzer sein, wenn der Kontext nicht pro Computer ist. *ProductCode* und *Kontext* Parameter sind erforderlich.

## <a name="members"></a>Member

Das **Product** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Product** -Objekt verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**Sourcelistaddmediadisk**](product-sourcelistaddmediadisk.md)       | Fügen Sie dem Satz registrierter Datenträger einen Datenträger hinzu.<br/>                                                              |
| [**Sourcelistaddsource**](product-sourcelistaddsource.md)             | Fügen Sie der Quell Liste eine Netzwerk-oder URL-Quelle hinzu.<br/>                                                         |
| [**Sourcelistclearall**](product-sourcelistclearall.md)               | Löscht die gesamte Quell Liste des angegebenen Quellen Typs.<br/>                                       |
| [**Sourcelistclearmediadisk**](product-sourcelistclearmediadisk.md)   | Entfernen Sie einen Datenträger aus der Gruppe der registrierten Datenträger aus der Quell Liste.<br/>                                    |
| [**Sourcelistclearsource**](product-sourcelistclearsource.md)         | Entfernen Sie eine Netzwerk-oder URL-Quelle aus der Quell Liste.<br/>                                                    |
| [**Sourcelistforceresolution**](product-sourcelistforceresolution.md) | Löscht die zuletzt verwendete Quelle. Dadurch wird eine Quell Listen Auflösung erzwungen, wenn die Quelle das nächste Mal benötigt wird.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **Product** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                      | BESCHREIBUNG                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Componentstate**](product-componentstate.md)<br/>   | Der Status einer angegebenen Komponente für diese Produkt Instanz. <br/>                   |
| [**Kontext**](product-context.md)<br/>                 | Der Kontext dieser Produkt Instanz als msiinstallcontext-Wert. <br/>                 |
| [**Featurestate**](product-featurestate.md)<br/>       | Der Status eines angegebenen Features für diese Produkt Instanz. <br/>                     |
| [**InstallProperty**](product-installproperty.md)<br/> | Der Wert einer angegebenen Eigenschaft. <br/>                                              |
| [**Mediadisks**](product-mediadisks.md)<br/>           | Listet alle Medien Datenträger für diese Produkt Instanz auf.<br/>                        |
| [**ProductCode**](product-productcode.md)<br/>         | Gibt den Produktcode zurück. <br/>                                                       |
| [**Sourcelistinfo**](product-sourcelistinfo.md)<br/>   | Informationen zu den Quell Informationen erhalten und festlegen Dies ist eine Lese-oder Schreib Eigenschaft.<br/> |
| [**Sources**](product-sources.md)<br/>                 | Listet alle Quellen für diese Produkt Instanz auf.<br/>                            |
| [**State**](product-state.md)<br/>                     | Der Installationsstatus des Produkts.<br/>                                               |
| [**UserSID**](product-usersid.md)<br/>                 | Gibt die Benutzer-SID zurück, unter der dieses Konto verfügbar ist.<br/>    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




