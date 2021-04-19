---
description: Für jedes Produkt, das im Patchpaket als berechtigt zum Empfangen des Patches aufgeführt ist, ruft die Applypatch-Methode des Installerobjekts eine Installation auf und legt die Patch-Eigenschaft auf den Pfad des Patchpakets fest.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Installer. Applypatch-Methode
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
ms.openlocfilehash: cc1b7509ddb4c61fa84a4547dcd47f2c7637b913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368542"
---
# <a name="installerapplypatch-method"></a>Installer. Applypatch-Methode

Für jedes Produkt, das im Patchpaket als berechtigt zum Empfangen des Patches aufgeführt ist, ruft die **Applypatch** -Methode des [**Installerobjekts**](installer-object.md) eine Installation auf und legt die [**Patch**](patch.md) -Eigenschaft auf den Pfad des Patchpakets fest.

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

*Patchpaket* 
</dt> <dd>

Gibt einen Pfad zum Patchpaket an.

</dd> <dt>

*INSTALLPACKAGE* 
</dt> <dd>

Wenn *InstallType* auf msiinstalltypetworkimage festgelegt ist, gibt *INSTALLPACKAGE* den Pfad zu dem Produkt an, das gepatcht werden soll. Wenn *InstallType* auf msiinstalltypedefault und *INSTALLPACKAGE* auf 0 festgelegt ist, wendet das Installationsprogramm den Patch auf jedes berechtigte Produkt an, das im Patchpaket aufgeführt ist.

Wenn *InstallType* den Wert msiinstalltypesingleinstance hat, wendet das Installationsprogramm den Patch auf das von *INSTALLPACKAGE* angegebene Produkt an. In diesem Fall werden andere im Patchpaket aufgelistete geeignete Produkte ignoriert, und der Parameter " *INSTALLPACKAGE* " enthält die auf NULL endenden Zeichenfolge, die den Produktcode der zu patchenden Instanz darstellt. Diese Art der Installation erfordert die Windows Installer Version, die in Windows Server 2003 oder höher oder Windows Installer XP SP1 oder höher enthalten ist.

</dd> <dt>

*InstallType* 
</dt> <dd>

Dieser Parameter gibt den Typ der zu patchenden Installation an. Der *InstallType* -Parameter wird ignoriert, wenn *INSTALLPACKAGE* ausgelassen wird.



| Wert                                                                                                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <dt>**msiinstalltypetworkimage**</dt> </dl> | Gibt eine administrative Installation an. In diesem Fall muss *INSTALLPACKAGE* auf einen Paketpfad festgelegt werden. Der Wert 1 für msiinstalltypetworkimage gibt eine administrative Installation an.<br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <dt>**msiinstalltypedefault**</dt> </dl>                     | Sucht das System nach Produkten, die gepatcht werden. In diesem Fall muss *INSTALLPACKAGE* eine leere Zeichenfolge sein.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <dt>**msiinstallsingleinstance**</dt> </dl>         | Patchen Sie das von *INSTALLPACKAGE* angegebene Produkt. *INSTALLPACKAGE* ist der Produktcode der zu patchenden Instanz. Diese Art der Installation erfordert die Windows Installer Version, die in Windows Server 2003 oder höher oder Windows Installer XP SP1 oder höher enthalten ist. Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> <dt>

*CommandLine* 
</dt> <dd>

Gibt die Eigenschaften Einstellungen an, die in der Befehlszeile festgelegt werden. Siehe Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Da das Listen Trennzeichen für Transformationen, Quellen und Patches ein Semikolon ist, sollte dieses Zeichen nicht für Dateinamen oder Pfade verwendet werden.

Die Eigenschaft [**Neuinstallation**](reinstall.md) ist erforderlich, wenn ein [kleines Update](small-updates.md) oder ein kleines [Upgradepatch](minor-upgrades.md) angewendet wird. Ohne diese Eigenschaft ist der Patch auf dem System registriert, kann aber keine Dateien aktualisieren.

**Windows Installer 2,0:** Sie müssen die Eigenschaft [**neu installieren**](reinstall.md) in der Befehlszeile festlegen, wenn Sie ein [kleines Update](small-updates.md) oder ein kleines [Upgradepatch](minor-upgrades.md) anwenden. Für Patches, die keinen [benutzerdefinierten Aktionstyp "51](custom-action-type-51.md) " verwenden, um die Eigenschaften " **REINSTALL** " und " [**REINSTALLMODE**](reinstallmode.md) " automatisch festzulegen, muss die Eigenschaft " **REINSTALL** " explizit mit dem *CommandLine* -Parameter festgelegt werden. Legen Sie die Eigenschaft **neu installieren** fest, um die vom Patch betroffenen Features aufzulisten, oder verwenden Sie die Standardeinstellung "REINSTALL = ALL". Der Standardwert der Eigenschaft **REINSTALLMODE** ist "omus".

**Windows Installer 3,0 und höher:** Ab Windows Installer Version 3,0 wird die Eigenschaft [**neu installieren**](reinstall.md) vom Installationsprogramm konfiguriert und muss nicht in der Befehlszeile festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[Informationen zu Eigenschaften](about-properties.md)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




