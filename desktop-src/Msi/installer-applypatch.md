---
description: Für jedes Produkt, das vom Patchpaket als für den Patch geeignet aufgeführt wird, ruft die ApplyPatch-Methode des Installer-Objekts eine Installation auf und legt die PATCH-Eigenschaft auf den Pfad des Patchpakets fest.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Installer.ApplyPatch-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c4bcb1ba1dc988f3c28188b4b448dba611b83c6cffbe7f942710569ac089776f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633227"
---
# <a name="installerapplypatch-method"></a>Installer.ApplyPatch-Methode

Für jedes Produkt, das vom Patchpaket als für den Patch geeignet aufgeführt wird, ruft die **ApplyPatch-Methode** des [**Installer-Objekts**](installer-object.md) eine Installation auf und legt die [**PATCH-Eigenschaft**](patch.md) auf den Pfad des Patchpakets fest.

## <a name="syntax"></a>Syntax


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PatchPackage* 
</dt> <dd>

Gibt einen Pfad zum Patchpaket an.

</dd> <dt>

*InstallPackage* 
</dt> <dd>

Wenn *InstallType* auf msiInstallTypeNetworkImage festgelegt ist, gibt *InstallPackage* den Pfad zum Produkt an, das gepatcht werden soll. Wenn *InstallType* auf msiInstallTypeDefault und *InstallPackage* auf 0 festgelegt ist, wendet das Installationsprogramm den Patch auf jedes geeignete Produkt an, das im Patchpaket aufgeführt ist.

Wenn *InstallType* msiInstallTypeSingleInstance ist, wendet das Installationsprogramm den Patch auf das produkt an, das von *InstallPackage* angegeben wird. In diesem Fall werden andere berechtigte Produkte, die im Patchpaket aufgeführt sind, ignoriert, und der *InstallPackage-Parameter* enthält die auf NULL endende Zeichenfolge, die den Produktcode der zu patchende Instanz darstellt. Für diese Art der Installation ist die Windows Installer-Version erforderlich, die mit Windows Server 2003 oder höher oder Windows Installer XP SP1 oder höher ausgeliefert wird.

</dd> <dt>

*InstallType* 
</dt> <dd>

Dieser Parameter gibt den Typ der installation an, die gepatcht werden soll. Der *InstallType-Parameter* wird ignoriert, wenn *InstallPackage* ausgelassen wird.



| Wert                                                                                                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <dt>**msiInstallTypeNetworkImage**</dt> </dl> | Gibt eine Administratorinstallation an. In diesem Fall muss *InstallPackage* auf einen Paketpfad festgelegt werden. Der Wert 1 für msiInstallTypeNetworkImage gibt eine Administratorinstallation an.<br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <dt>**msiInstallTypeDefault**</dt> </dl>                     | Durchsucht das System nach zu patchende Produkte. In diesem Fall muss *InstallPackage* eine leere Zeichenfolge sein.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <dt>**msiInstallSingleInstance**</dt> </dl>         | Patchen Sie das von *InstallPackage* angegebene Produkt. *InstallPackage* ist der Produktcode der instanz, die gepatcht werden soll. Diese Art der Installation erfordert die Windows Installer-Version, die mit Windows Server 2003 oder höher oder Windows Installer XP SP1 oder höher ausgeliefert wird. Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches.](installing-multiple-instances-of-products-and-patches.md)<br/> |



 

</dd> <dt>

*CommandLine* 
</dt> <dd>

Gibt eigenschafteneinstellungen an, die in der Befehlszeile festgelegt werden. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Da das Listentrennzeichen für Transformationen, Quellen und Patches ein Semikolon ist, sollte dieses Zeichen nicht für Dateinamen oder Pfade verwendet werden.

Die [**REINSTALL-Eigenschaft**](reinstall.md) ist erforderlich, wenn ein [kleines Update](small-updates.md) oder ein kleiner [Upgradepatch](minor-upgrades.md) angewendet wird. Ohne diese Eigenschaft wird der Patch auf dem System registriert, kann aber keine Dateien aktualisieren.

**Windows Installer 2.0:** Sie müssen die [**REINSTALL-Eigenschaft**](reinstall.md) in der Befehlszeile festlegen, wenn Sie ein [kleines Update](small-updates.md) oder [einen kleineren Upgradepatch](minor-upgrades.md) anwenden. Für Patches, die keinen [benutzerdefinierten Aktionstyp 51](custom-action-type-51.md) verwenden, um die Eigenschaften **REINSTALL** und [**REINSTALLMODE**](reinstallmode.md) automatisch festzulegen, muss die **REINSTALL-Eigenschaft** explizit mit dem *CommandLine-Parameter* festgelegt werden. Legen Sie die **REINSTALL-Eigenschaft** fest, um die vom Patch betroffenen Features aufzulisten, oder verwenden Sie die praktische Standardeinstellung "REINSTALL=ALL". Der Standardwert der **REINSTALLMODE-Eigenschaft** ist "omus".

**Windows Installer 3.0 und höher:** Ab Windows Installer Version 3.0 wird die [**REINSTALL-Eigenschaft**](reinstall.md) vom Installationsprogramm konfiguriert und muss nicht in der Befehlszeile festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 3.0 oder höher auf Windows Server 2003 oder Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[Informationen zu Eigenschaften](about-properties.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




