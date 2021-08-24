---
description: Die InstallProperty-Eigenschaft ist der Wert der -Eigenschaft für die Instanz dieses Produkts. Diese Eigenschaft ruft die MsiGetProductInfoEx-Funktion mit ProductCode, UserSid und Context des Product-Objekts und der angeforderten Eigenschaft als Parameter auf.
ms.assetid: 945c11fe-39da-43b7-a19f-e6364d5e715c
title: Product.InstallProperty-Methode
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
ms.openlocfilehash: 3beb67ccdd4a50cdbb52e41846f46fcb4f2545dd833d30098e29c4d5887f8fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926070"
---
# <a name="productinstallproperty-method"></a>Product.InstallProperty-Methode

Die **InstallProperty-Eigenschaft** ist der Wert der -Eigenschaft für die Instanz dieses Produkts.

Diese Eigenschaft ruft die [**MsiGetProductInfoEx-Funktion**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) mit *productCode,* *UserSid* und *Context* des [**Product-Objekts**](product-object.md) und der angeforderten Eigenschaft als Parameter auf.

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

Gibt die abzurufende Eigenschaft an. Die Eigenschaften in der folgenden Liste können nur von Anwendungen abgerufen werden, die bereits installiert sind. Beachten [Sie, dass](required-properties.md) die erforderlichen Eigenschaften garantiert verfügbar sind, andere Eigenschaften jedoch nur verfügbar sind, wenn diese Eigenschaft festgelegt wurde. Informationen dazu, wie die einzelnen Eigenschaften [festgelegt](properties.md) werden, finden Sie unter den angegebenen Links zu den Eigenschaften des Installationsprogramms.



| Installierte Eigenschaften                                                                                                                                                                                                               | Bedeutung                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INSTALLPROPERTY_PRODUCTSTATE"></span><span id="installproperty_productstate"></span><dl> <dt>**INSTALLPROPERTY \_ PRODUCTSTATE**</dt> </dl>                         | Der Status des Produkts, das in Zeichenfolgenform als "1" für Angekündigt und "5" für installiert zurückgegeben wird.<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_HELPLINK"></span><span id="installproperty_helplink"></span><dl> <dt>**INSTALLPROPERTY \_ HELPLINK**</dt> </dl>                                     | Supportlink. Weitere Informationen finden Sie unter der [**ARPHELPLINK-Eigenschaft.**](arphelplink.md)<br/>                                                                                                                                                                                                                                                                             |
| <span id="INSTALLPROPERTY_HELPTELEPHONE"></span><span id="installproperty_helptelephone"></span><dl> <dt>**INSTALLPROPERTY \_ HELPTELEPHONE**</dt> </dl>                      | Supporttelefon. Weitere Informationen finden Sie unter der [**ARPHELPTELEPHONE-Eigenschaft.**](arphelptelephone.md)<br/>                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_INSTALLDATE"></span><span id="installproperty_installdate"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLDATE**</dt> </dl>                            | Der Zeitpunkt, zu dem dieses Produkt den Dienst zuletzt empfangen hat. Der Wert dieser Eigenschaft wird jedes Mal ersetzt, wenn ein Patch [](command-line-options.md) angewendet oder aus dem Produkt entfernt wird oder die /v-Befehlszeilenoption verwendet wird, um das Produkt zu reparieren. Wenn das Produkt keine Reparaturen oder Patches erhalten hat, enthält diese Eigenschaft den Zeitpunkt, zu dem dieses Produkt auf diesem Computer installiert wurde.<br/> |
| <span id="INSTALLPROPERTY_INSTALLEDPRODUCTNAME"></span><span id="installproperty_installedproductname"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLEDPRODUCTNAME**</dt> </dl> | Name des installierten Produkts. Weitere Informationen finden Sie unter der [**ProductName-Eigenschaft.**](productname.md)<br/>                                                                                                                                                                                                                                                                   |
| <span id="INSTALLPROPERTY_INSTALLLOCATION"></span><span id="installproperty_installlocation"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLLOCATION**</dt> </dl>                | Installationsspeicherort. Weitere Informationen finden Sie unter der [**ARPINSTALLLOCATION-Eigenschaft.**](arpinstalllocation.md)<br/>                                                                                                                                                                                                                                                      |
| <span id="INSTALLPROPERTY_INSTALLSOURCE"></span><span id="installproperty_installsource"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLSOURCE**</dt> </dl>                      | Installationsquelle. Weitere Informationen finden Sie unter der [**SourceDir-Eigenschaft.**](sourcedir.md)<br/>                                                                                                                                                                                                                                                                          |
| <span id="INSTALLPROPERTY_LOCALPACKAGE"></span><span id="installproperty_localpackage"></span><dl> <dt>**INSTALLPROPERTY \_ LOCALPACKAGE**</dt> </dl>                         | Lokal zwischengespeichertes Paket.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="INSTALLPROPERTY_PUBLISHER"></span><span id="installproperty_publisher"></span><dl> <dt>**INSTALLPROPERTY \_ PUBLISHER**</dt> </dl>                                  | Publisher. Weitere Informationen finden Sie in der [**Manufacturer-Eigenschaft.**](manufacturer.md)<br/>                                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_URLINFOABOUT"></span><span id="installproperty_urlinfoabout"></span><dl> <dt>**INSTALLPROPERTY \_ URLINFOABOUT**</dt> </dl>                         | URL-Informationen. Weitere Informationen finden Sie unter der [**ARPURLINFOABOUT-Eigenschaft.**](arpurlinfoabout.md)<br/>                                                                                                                                                                                                                                                                  |
| <span id="INSTALLPROPERTY_URLUPDATEINFO"></span><span id="installproperty_urlupdateinfo"></span><dl> <dt>**INSTALLPROPERTY \_ URLUPDATEINFO**</dt> </dl>                      | URL-Updateinformationen. Weitere Informationen finden Sie unter der [**ARPURLUPDATEINFO-Eigenschaft.**](arpurlupdateinfo.md)<br/>                                                                                                                                                                                                                                                         |
| <span id="INSTALLPROPERTY_VERSIONMINOR"></span><span id="installproperty_versionminor"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONMINOR**</dt> </dl>                         | Nebenproduktversion, die von der [**ProductVersion-Eigenschaft abgeleitet**](productversion.md) wird.<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONMAJOR"></span><span id="installproperty_versionmajor"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONMAJOR**</dt> </dl>                         | Hauptproduktversion, die von der [**ProductVersion-Eigenschaft abgeleitet**](productversion.md) ist.<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONSTRING"></span><span id="installproperty_versionstring"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONSTRING**</dt> </dl>                      | Die Produktversion. Weitere Informationen finden Sie unter der [**ProductVersion-Eigenschaft.**](productversion.md)<br/>                                                                                                                                                                                                                                                                    |



 

Um die Produkt-ID, den registrierten Besitzer oder das registrierte  Unternehmen aus bereits installierten Anwendungen abzurufen, legen Sie die -Eigenschaft auf einen der folgenden Textzeichenfolgenwerte fest.



| Wert      | BESCHREIBUNG                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| ProductID  | Der Produktbezeichner. Weitere Informationen finden Sie unter der [**ProductID-Eigenschaft.**](productid.md) |
| RegCompany | Das Unternehmen, das für die Verwendung dieses Produkts registriert ist.                                                    |
| RegOwner   | Der für die Verwendung dieses Produkts registrierte Besitzer.                                                      |



 

Legen Sie die -Eigenschaft auf  den folgenden Wert fest, um den Instanztyp des Produkts abzurufen. Diese Eigenschaft ist für angekündigte oder installierte Produkte verfügbar.



| Wert        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InstanceType | Ein fehlender Wert oder der Wert 0 gibt eine normale Produktinstallation an. Der Wert 1 gibt ein Produkt an, das mithilfe einer Transformation mit mehreren Instanzen und der [**MSINEWINSTANCE-Eigenschaft installiert**](msinewinstance.md) wurde. Verfügbar mit dem Installationsprogramm unter Windows Server 2003 oder Windows XP mit SP1. Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches.](installing-multiple-instances-of-products-and-patches.md) |



 

Die Eigenschaften in der folgenden Liste können auch aus angekündigten Anwendungen abgerufen werden. Diese Eigenschaften können nicht für Produktinstanzen abgerufen werden, die in einem benutzerspezifischen, nicht verwalteten Kontext für andere Benutzerkonten als das aktuelle Benutzerkonto installiert werden.



| Angekündigte Eigenschaften                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                          |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_INSTALLPROPERTY-TRANSFORMATIONEN           | Transformationen:                                                                                                                                                                                                                                                                                          |
| \_INSTALLPROPERTY-SPRACHE             | Produktsprache.                                                                                                                                                                                                                                                                                    |
| INSTALLPROPERTY \_ PRODUCTNAME          | Lesbar für Menschen– Produktname. Weitere Informationen finden Sie unter der [**ProductName-Eigenschaft.**](productname.md)                                                                                                                                                                                              |
| INSTALLPROPERTY \_ ASSIGNMENTTYPE       | Entspricht 0 (null), wenn das Produkt pro Benutzer angekündigt oder installiert wird. Entspricht 1 ( 1), wenn das Produkt pro Computer für alle Benutzer angekündigt oder installiert wird.<br/>                                                                                                                                  |
| INSTALLPROPERTY \_ PACKAGECODE          | Bezeichner des Pakets, aus dem dieses Produkt installiert wurde. Weitere Informationen finden Sie unter [Paketcodes](package-codes.md).                                                                                                                                                                                      |
| INSTALLPROPERTY-VERSION \_              | Von der [**ProductVersion-Eigenschaft abgeleitete Produktversion.**](productversion.md)                                                                                                                                                                                                                  |
| INSTALLPROPERTY \_ PRODUCTICON          | Primäres Symbol für das Paket. Weitere Informationen finden Sie unter der [**ARPPRODUCTICON-Eigenschaft.**](arpproducticon.md)                                                                                                                                                                                       |
| INSTALLPROPERTY \_ PACKAGENAME          | Name des ursprünglichen Installationspakets.                                                                                                                                                                                                                                                           |
| INSTALLPROPERTY \_ AUTHORIZED \_ LUA \_ APP | Der Wert 1 gibt ein Produkt an, das von Nichtadministratoren mithilfe des UAC-Patchings [(User Account Control, Benutzerkontensteuerung) verwaltet werden kann.](user-account-control--uac--patching.md) Ein fehlender Wert oder der Wert 0 gibt an, dass das Patchen mit den geringsten Rechten nicht aktiviert ist. Verfügbar mit Windows Installer 3.0 und höher. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn der Aufruf erfolgreich ist, enthält die -Eigenschaft den Wert als Zeichenfolge.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct ist als 000C10A0-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Produkt**](product-object.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




