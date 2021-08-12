---
description: Die CreateAdvertiseScript-Methode des Installer-Objekts generiert ein Anklangskript.
ms.assetid: 32a331e5-d291-49cd-ab0e-7d0e4d72a95b
title: Installer::CreateAdvertiseScript-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateAdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9416b3b503db11411db93c66242ea55587e6175344313f785c08392c72ad0991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631956"
---
# <a name="installercreateadvertisescript-method"></a>Installer::CreateAdvertiseScript-Methode

Die **CreateAdvertiseScript-Methode** des [**Installer-Objekts**](installer-object.md) generiert ein Anklangskript.

## <a name="syntax"></a>Syntax


```JScript
.CreateAdvertiseScript(
  packagePath,
  scriptFilePath,
  transforms,
  language,
  platform,
  options
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*packagePath* 
</dt> <dd>

Der vollständige Pfad zum Windows Installer-Paket (.msi), das angekündigt werden soll.

</dd> <dt>

*scriptFilePath* 
</dt> <dd>

Der vollständige Pfad zur Skriptdatei, die mit den angekündigten Informationen erstellt werden soll.

</dd> <dt>

*Verwandelt* 
</dt> <dd>

Die Liste der Transformationen, die auf das Produkt angewendet werden. Transformationen in der Liste werden durch Semikolons getrennt. Dieser Parameter ist optional.

</dd> <dt>

*language* 
</dt> <dd>

Die Sprache des zu verwendenden Installationspakets. Dieser Parameter ist optional.

</dd> <dt>

*platform* 
</dt> <dd>

Dieser Parameter gibt an, für welche Plattform das Installationsprogramm das Skript erstellen soll. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                                       | Bedeutung                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="msiAdvertiseCurrentPlatform"></span><span id="msiadvertisecurrentplatform"></span><span id="MSIADVERTISECURRENTPLATFORM"></span><dl> <dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt> </dl> | Erstellt ein Skript für die aktuelle Plattform.<br/>  |
| <span id="msiAdvertiseX86Platform"></span><span id="msiadvertisex86platform"></span><span id="MSIADVERTISEX86PLATFORM"></span><dl> <dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt> </dl>                 | Erstellt ein Skript für die x86-Plattform.<br/>      |
| <span id="msiAdvertiseIA64Platform"></span><span id="msiadvertiseia64platform"></span><span id="MSIADVERTISEIA64PLATFORM"></span><dl> <dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt> </dl>             | Erstellt ein Skript für Itanium-basierte Systeme.<br/> |
| <span id="msiAdvertiseX64Platform"></span><span id="msiadvertisex64platform"></span><span id="MSIADVERTISEX64PLATFORM"></span><dl> <dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt> </dl>                 | Erstellt ein Skript für die x64-Plattform.<br/>      |



 

</dd> <dt>

*options* 
</dt> <dd>

Ankündigungsoptionen. Dieser Parameter ist optional. Dieser Parameter kann einen der folgenden Werte annehmen. Dieser Parameter ist optional.



| Wert                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**msiAdvertiseDefault**</dt> <dt>0</dt> </dl>                             | Standard-Ankündigung<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt> </dl> | Gibt eine neue Instanz des Produkts an. Erfordert, dass die erste Transformation in der *Transformationsliste des Transformationsparameters* die Instanztransformation ist, die den Produktcode ändert. Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches.](installing-multiple-instances-of-products-and-patches.md)<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**AdvertiseProduct-Methode**](installer-advertiseproduct.md) verwendet die [**MsiAdvertiseProductEx-Funktion.**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **CreateAdvertiseScript-Methode** veranschaulicht.


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Create an advertise script for Orca
'

Installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scripts\orca.aas"
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 4.5 auf Windows Server 2003 und Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Installer**](installer-object.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 3.1 und früheren Versionen](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




