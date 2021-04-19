---
description: Mit der Methode "konfigurierte Funktion" des Installerobjekts wird der installierte Zustand einer Produkt Funktion konfiguriert.
ms.assetid: cc950951-3b43-4d86-9ff1-80aa2ccd11d5
title: Installer.Configurefeature-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 737019f5c404beabef404751e617be975b946c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370868"
---
# <a name="installerconfigurefeature-method"></a>Installer.Configurefeature-Methode

Mit der Methode " **konfigurierte Funktion" des Installerobjekts** wird der installierte Zustand einer Produkt Funktion konfiguriert. [](installer-object.md)

## <a name="syntax"></a>Syntax


```JScript
Installer.ConfigureFeature(
  Product,
  Feature,
  InstallState
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Produkt* 
</dt> <dd>

Gibt den Produktcode des Produkts an.

</dd> <dt>

*Feature* 
</dt> <dd>

Gibt die Funktions-ID der Funktion an, die konfiguriert werden soll.

</dd> <dt>

*InstallState* 
</dt> <dd>

Gibt den Installationsstatus für das Feature an. Dieser Parameter muss einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                        | Bedeutung                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <dt>**msiinstallstateangekündigten**</dt> </dl> | Die Funktion wird angekündigt.<br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <dt>**msiinstallstatuelocal**</dt> </dl>                     | Das Feature wird lokal installiert.<br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <dt>**msiinstallstatemissing**</dt> </dl>                 | Die Funktion ist deinstalliert.<br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <dt>**msiinstallstaatource**</dt> </dl>                 | Das Feature wird zum Ausführen von der Quelle installiert.<br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <dt>**msiinstallstatedefault**</dt> </dl>             | Die Funktion wird am Standard Speicherort installiert.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msikonfigurierfeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[Installations-und Konfigurationsfunktionen](installer-function-reference.md)
</dt> </dl>

 

 




