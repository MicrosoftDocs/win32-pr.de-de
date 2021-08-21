---
description: Die ConfigureProduct-Methode des Installer-Objekts installiert oder deinstalliert ein Produkt.
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Installer.ConfigureProduct-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7fd64424105bc06364abf2b047ba4d986fdd5540d007109dfb9fdc087250c194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632157"
---
# <a name="installerconfigureproduct-method"></a>Installer.ConfigureProduct-Methode

Die **ConfigureProduct-Methode** des [**Installer-Objekts**](installer-object.md) installiert oder deinstalliert ein Produkt.

## <a name="syntax"></a>Syntax


```JScript
Installer.ConfigureProduct(
  Product,
  InstallLevel,
  InstallState
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Produkt* 
</dt> <dd>

Gibt den Produktcode des Produkts an.

</dd> <dt>

*InstallLevel* 
</dt> <dd>

Gibt die Standardinstallationskonfiguration des Produkts an. Der InstallLevel-Parameter wird ignoriert, und alle Funktionen werden installiert, wenn der InstallState-Parameter auf einen anderen Wert als msiInstallStateDefault festgelegt ist.

Dieser Parameter muss entweder 0 (installation mit erstellten Featureebenen), 65535 (Alle Features installieren) oder einen Wert zwischen 0 und 65535 aufweisen, um eine Teilmenge der verfügbaren Features zu installieren.

</dd> <dt>

*InstallState* 
</dt> <dd>

Gibt den Installationsstatus für das Feature an. Dieser Parameter muss einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                        | Bedeutung                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <dt>**msiInstallStateAdvertised**</dt> </dl> | Das Feature wird angekündigt.<br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <dt>**msiInstallStateLocal**</dt> </dl>                     | Das Feature wird lokal installiert.<br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <dt>**msiInstallStateAbsent**</dt> </dl>                 | Das Feature wird deinstalliert.<br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <dt>**msiInstallStateSource**</dt> </dl>                 | Das Feature wird installiert, um von der Quelle aus ausgeführt zu werden.<br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <dt>**msiInstallStateDefault**</dt> </dl>             | Das Feature wird am Standardspeicherort installiert.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **ConfigureProduct-Methode** zeigt die Benutzeroberfläche mit aktuellen Einstellungen an. Benutzeroberflächeneinstellungen können geändert werden, indem die [**UILevel-Eigenschaft (Installer-Objekt)**](installer-uilevel.md) vor dem Aufrufen der **ConfigureProduct-Methode** geändert wird.

Wenn der *InstallState-Parameter* auf einen anderen Wert als msiInstallStateDefault festgelegt ist, wird der *InstallLevel-Parameter* ignoriert, und alle Features des Produkts werden installiert. Verwenden Sie die [**ConfigureFeature-Methode,**](installer-configurefeature.md) um die Installation einzelner Features zu steuern, wenn der *InstallState-Parameter* nicht auf msiInstallStateDefault festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[Installations- und Konfigurationsfunktionen](installer-function-reference.md)
</dt> </dl>

 

 




