---
description: Die InstallProperty-Eigenschaft ist der Wert der-Eigenschaft für die Instanz dieses Produkts. Diese Eigenschaft ruft die msigetproductinfoex-Funktion auf, wobei ProductCode, UserSID und der Kontext des Product-Objekts und die angeforderte Eigenschaft als Parameter verwendet werden.
ms.assetid: 945c11fe-39da-43b7-a19f-e6364d5e715c
title: Product. InstallProperty-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.InstallProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12949997363fce8073c15f7ca6b7312c211fa0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370000"
---
# <a name="productinstallproperty-method"></a>Product. InstallProperty-Methode

Die **InstallProperty** -Eigenschaft ist der Wert der-Eigenschaft für die Instanz dieses Produkts.

Diese Eigenschaft ruft die [**msigetproductinfoex**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) -Funktion auf, wobei *ProductCode*, *UserSID* und der *Kontext* des [**Product**](product-object.md) -Objekts und die angeforderte Eigenschaft als Parameter verwendet werden.

## <a name="syntax"></a>Syntax


```JScript
Product.InstallProperty(
  property
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*property* 
</dt> <dd>

Gibt die Eigenschaft an, die abgerufen werden soll. Die Eigenschaften in der folgenden Liste können nur aus Anwendungen abgerufen werden, die bereits installiert sind. Beachten Sie, dass [erforderliche](required-properties.md) Eigenschaften garantiert verfügbar sind. andere Eigenschaften sind jedoch nur verfügbar, wenn diese Eigenschaft festgelegt wurde. Informationen zur Festlegung der einzelnen Eigenschaften finden Sie unter den aufgeführten Links zu den [installereigenschaften](properties.md) .



| Installierte Eigenschaften                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INSTALLPROPERTY_PRODUCTSTATE"></span><span id="installproperty_productstate"></span><dl> <dt>**InstallProperty \_ productstate**</dt> </dl>                         | Status des Produkts, das in der Zeichenfolge als "1" für angekündigte und "5" für installiert zurückgegeben wurde.<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_HELPLINK"></span><span id="installproperty_helplink"></span><dl> <dt>**InstallProperty \_ HelpLink**</dt> </dl>                                     | Support Link. Weitere Informationen finden Sie unter der [**arphelplink**](arphelplink.md) -Eigenschaft.<br/>                                                                                                                                                                                                                                                                             |
| <span id="INSTALLPROPERTY_HELPTELEPHONE"></span><span id="installproperty_helptelephone"></span><dl> <dt>**InstallProperty \_ Help Telefon**</dt> </dl>                      | Support Telefon. Weitere Informationen finden Sie unter der [**arphelptelefon**](arphelptelephone.md) -Eigenschaft.<br/>                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_INSTALLDATE"></span><span id="installproperty_installdate"></span><dl> <dt>**InstallProperty \_ InstallDate**</dt> </dl>                            | Der letzte Zeitpunkt, zu dem dieser Produkt Dienst empfangen hat. Der Wert dieser Eigenschaft wird bei jedem anwenden oder Entfernen eines Patches aus dem Produkt ersetzt, oder die [Befehlszeilen Option](command-line-options.md) /v wird verwendet, um das Produkt zu reparieren. Wenn das Produkt keine Reparaturen oder Patches erhalten hat, enthält diese Eigenschaft den Zeitpunkt, zu dem dieses Produkt auf diesem Computer installiert wurde.<br/> |
| <span id="INSTALLPROPERTY_INSTALLEDPRODUCTNAME"></span><span id="installproperty_installedproductname"></span><dl> <dt>**InstallProperty \_ installedproductname**</dt> </dl> | Installierter Produktname. Weitere Informationen finden Sie unter der [**ProductName**](productname.md) -Eigenschaft.<br/>                                                                                                                                                                                                                                                                   |
| <span id="INSTALLPROPERTY_INSTALLLOCATION"></span><span id="installproperty_installlocation"></span><dl> <dt>**INSTALLLOCATION \_ InstallLocation**</dt> </dl>                | Installationsort. Weitere Informationen finden Sie unter der [**arpinstalllocation**](arpinstalllocation.md) -Eigenschaft.<br/>                                                                                                                                                                                                                                                      |
| <span id="INSTALLPROPERTY_INSTALLSOURCE"></span><span id="installproperty_installsource"></span><dl> <dt>**InstallProperty \_ InstallSource**</dt> </dl>                      | Installationsquelle: Weitere Informationen finden Sie unter der [**SourceDir**](sourcedir.md) -Eigenschaft.<br/>                                                                                                                                                                                                                                                                          |
| <span id="INSTALLPROPERTY_LOCALPACKAGE"></span><span id="installproperty_localpackage"></span><dl> <dt>**InstallProperty \_ localpackage**</dt> </dl>                         | Lokales zwischengespeichertes Paket.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="INSTALLPROPERTY_PUBLISHER"></span><span id="installproperty_publisher"></span><dl> <dt>**InstallProperty- \_ Verleger**</dt> </dl>                                  | Gebers. Weitere Informationen finden Sie unter der Eigenschaft " [**Hersteller**](manufacturer.md) ".<br/>                                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_URLINFOABOUT"></span><span id="installproperty_urlinfoabout"></span><dl> <dt>**InstallProperty \_ urlinfoabout**</dt> </dl>                         | URL-Informationen. Weitere Informationen finden Sie unter der [**arpurlinfoabout**](arpurlinfoabout.md) -Eigenschaft.<br/>                                                                                                                                                                                                                                                                  |
| <span id="INSTALLPROPERTY_URLUPDATEINFO"></span><span id="installproperty_urlupdateinfo"></span><dl> <dt>**InstallProperty \_ urlupdateinfo**</dt> </dl>                      | URL-Update Informationen. Weitere Informationen finden Sie unter der [**arpurlupdateinfo**](arpurlupdateinfo.md) -Eigenschaft.<br/>                                                                                                                                                                                                                                                         |
| <span id="INSTALLPROPERTY_VERSIONMINOR"></span><span id="installproperty_versionminor"></span><dl> <dt>**InstallProperty \_ VersionMinor**</dt> </dl>                         | Nebenprodukt Version, die von der [**ProductVersion**](productversion.md) -Eigenschaft abgeleitet wird.<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONMAJOR"></span><span id="installproperty_versionmajor"></span><dl> <dt>**InstallProperty \_ VersionMajor**</dt> </dl>                         | Die hauptproduktversion, die von der [**ProductVersion**](productversion.md) -Eigenschaft abgeleitet wird.<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONSTRING"></span><span id="installproperty_versionstring"></span><dl> <dt>**InstallProperty \_ VersionString**</dt> </dl>                      | Die Produktversion. Weitere Informationen finden Sie unter der [**ProductVersion**](productversion.md) -Eigenschaft.<br/>                                                                                                                                                                                                                                                                    |



 

Legen Sie die- *Eigenschaft* auf einen der folgenden Textzeichen folgen Werte fest, um die Produkt-ID, den registrierten Besitzer oder das registrierte Unternehmen aus bereits installierten Anwendungen abzurufen.



| Wert      | BESCHREIBUNG                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| ProductID  | Der Produkt Bezeichner. Weitere Informationen finden Sie in der [**ProductID-**](productid.md) Eigenschaft. |
| RegCompany | Das Unternehmen, das zur Verwendung dieses Produkts registriert ist.                                                    |
| RegOwner   | Der Besitzer, der für die Verwendung dieses Produkts registriert ist.                                                      |



 

Um den Instanztyp des Produkts abzurufen, legen Sie die- *Eigenschaft* auf den folgenden Wert fest. Diese Eigenschaft ist für angekündigte oder installierte Produkte verfügbar.



| Wert        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InstanceType | Ein fehlender Wert oder der Wert 0 steht für eine normale Produktinstallation. Der Wert 1 gibt an, dass ein Produkt mit einer Transformation für mehrere Instanzen und der [**msinewinstance**](msinewinstance.md) -Eigenschaft installiert wurde. Verfügbar mit dem Installationsprogramm, auf dem Windows Server 2003 oder Windows XP mit SP1 ausgeführt wird. Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md). |



 

Die Eigenschaften in der folgenden Liste können auch von angekündigten Anwendungen abgerufen werden. Diese Eigenschaften können nicht für Produkt Instanzen abgerufen werden, die unter einem nicht verwalteten Benutzerkonto für Benutzerkonten mit Ausnahme des aktuellen Benutzerkontos installiert werden.



| Angekündigte Eigenschaften                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                          |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InstallProperty- \_ Transformationen           | Transformationen:                                                                                                                                                                                                                                                                                          |
| InstallProperty- \_ Sprache             | Produktsprache.                                                                                                                                                                                                                                                                                    |
| InstallProperty \_ ProductName          | Menschen lesbar – Produktname. Weitere Informationen finden Sie unter der [**ProductName**](productname.md) -Eigenschaft.                                                                                                                                                                                              |
| InstallProperty- \_ zutragungstyp       | Entspricht 0 (null), wenn das Produkt angekündigt oder pro Benutzer installiert wird. Entspricht eins (1), wenn das Produkt für alle Benutzer pro Computer angekündigt oder installiert wird.<br/>                                                                                                                                  |
| InstallProperty \_ PackageCode          | Der Bezeichner des Pakets, von dem dieses Produkt installiert wurde. Weitere Informationen finden Sie unter [Paket Codes](package-codes.md).                                                                                                                                                                                      |
| InstallProperty- \_ Version              | Die Produktversion, die von der [**ProductVersion**](productversion.md) -Eigenschaft abgeleitet wird.                                                                                                                                                                                                                  |
| InstallProperty \_ producticon          | Primäres Symbol für das Paket. Weitere Informationen finden Sie unter der [**arpproducticon**](arpproducticon.md) -Eigenschaft.                                                                                                                                                                                       |
| InstallProperty \_ PackageName          | Der Name des ursprünglichen Installationspakets.                                                                                                                                                                                                                                                           |
| InstallProperty \_ autorisierte \_ Lua- \_ App | Der Wert 1 gibt ein Produkt an, das von nicht Administratoren mithilfe von [Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md)gewartet werden kann. Ein fehlender Wert oder der Wert 0 gibt an, dass das Patchen mit den geringsten Berechtigungen nicht aktiviert ist. Verfügbar mit Windows Installer 3,0 und höher. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der-Befehl erfolgreich ausgeführt wird, enthält die-Eigenschaft den Wert als Zeichenfolge.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Product**](product-object.md)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




