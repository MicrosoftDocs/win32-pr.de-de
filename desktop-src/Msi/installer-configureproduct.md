---
description: Mit der Methode "Konfigurations Methode" des Installerobjekts wird ein Produkt installiert oder deinstalliert.
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Installer.Configureproduct-Methode
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
ms.openlocfilehash: 989855508215b2cd5d04bff7903628513314b9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361077"
---
# <a name="installerconfigureproduct-method"></a>Installer.Configureproduct-Methode

Mit der Methode "Konfigurations Methode" des **Installerobjekts** wird ein Produkt installiert oder deinstalliert. [](installer-object.md)

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

Gibt die Standardkonfiguration für die Installation des Produkts an. Der Parameter "INSTALLLEVEL" wird ignoriert, und alle Funktionen werden installiert, wenn der Parameter "InstallState" auf einen anderen Wert als "msiinstallstatedefault" festgelegt ist.

Dieser Parameter muss entweder 0 (Installation mithilfe der erstellten Funktionsebenen), 65535 (alle Features installieren) oder ein Wert zwischen 0 und 65535 sein, um eine Teilmenge der verfügbaren Features zu installieren.

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

## <a name="remarks"></a>Bemerkungen

Die Methode " **Konfigurations** Methode" zeigt die Benutzeroberfläche mithilfe der aktuellen Einstellungen an. Die Benutzeroberflächen Einstellungen können geändert werden, indem Sie die [**uilevel-Eigenschaft (Installer-Objekt)**](installer-uilevel.md) vor dem Aufrufen der Methode " **Konfigurations** Methode" ändern.

Wenn der Parameter " *InstallState* " auf einen anderen Wert als "msiinstallstatedefault" festgelegt ist, wird der Parameter " *INSTALLLEVEL* " ignoriert, und alle Features des Produkts werden installiert. Verwenden Sie die Methode " [**Konfigurierung**](installer-configurefeature.md) ", um die Installation einzelner Funktionen zu steuern, wenn der Parameter " *InstallState* " nicht auf "msiinstallstatedefault" festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msikonfigurireproduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[Installations-und Konfigurationsfunktionen](installer-function-reference.md)
</dt> </dl>

 

 




