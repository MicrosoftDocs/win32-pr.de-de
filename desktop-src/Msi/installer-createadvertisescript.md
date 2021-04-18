---
description: Mit der Methode "-Methode" der Methode "-Installer" wird ein Ankündigungs Skript generiert.
ms.assetid: 32a331e5-d291-49cd-ab0e-7d0e4d72a95b
title: 'Installer:: kreatewerbung-Methode'
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
ms.openlocfilehash: 9ec4b18eee376e7bde4824a497ea14b503045f43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358155"
---
# <a name="installercreateadvertisescript-method"></a>Installer:: kreatewerbung-Methode

Mit **der Methode "** -Methode" der Methode "- [**Installer**](installer-object.md) " wird ein Ankündigungs Skript generiert.

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

Der vollständige Pfad zum Windows Installer Paket (. msi), das angekündigt werden soll.

</dd> <dt>

*ScriptFilePath* 
</dt> <dd>

Der vollständige Pfad zu der Skriptdatei, die mit den angekündigten Informationen erstellt werden soll.

</dd> <dt>

*Kranz* 
</dt> <dd>

Die Liste der Transformationen, die auf das Produkt angewendet werden sollen. Transformationen in der Liste werden durch Semikolons getrennt. Dieser Parameter ist optional.

</dd> <dt>

*language* 
</dt> <dd>

Die Sprache des zu verwendenden Installationspakets. Dieser Parameter ist optional.

</dd> <dt>

*platform* 
</dt> <dd>

Dieser Parameter gibt an, für welche Plattform das Installationsprogramm vom Installationsprogramm erstellt werden soll. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                                       | Bedeutung                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="msiAdvertiseCurrentPlatform"></span><span id="msiadvertisecurrentplatform"></span><span id="MSIADVERTISECURRENTPLATFORM"></span><dl> <dt>**msiankündigen-currentplatform**</dt> <dt>0</dt> </dl> | Erstellt ein Skript für die aktuelle Plattform.<br/>  |
| <span id="msiAdvertiseX86Platform"></span><span id="msiadvertisex86platform"></span><span id="MSIADVERTISEX86PLATFORM"></span><dl> <dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt> </dl>                 | Erstellt ein Skript für die x86-Plattform.<br/>      |
| <span id="msiAdvertiseIA64Platform"></span><span id="msiadvertiseia64platform"></span><span id="MSIADVERTISEIA64PLATFORM"></span><dl> <dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt> </dl>             | Erstellt ein Skript für Itanium-basierte Systeme.<br/> |
| <span id="msiAdvertiseX64Platform"></span><span id="msiadvertisex64platform"></span><span id="MSIADVERTISEX64PLATFORM"></span><dl> <dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt> </dl>                 | Erstellt ein Skript für die x64-Plattform.<br/>      |



 

</dd> <dt>

*options* 
</dt> <dd>

Ankündigungs Optionen. Dieser Parameter ist optional. Dieser Parameter kann einen der folgenden Werte annehmen. Dieser Parameter ist optional.



| Wert                                                                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**msiankündigen-Standard**</dt> Wert <dt>0</dt> </dl>                             | Standard Ankündigung<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**msiwerbesesinglabstance**</dt> <dt>1</dt> </dl> | Gibt eine neue Instanz des Produkts an. Erfordert, dass die erste Transformation in der Transformations Liste des *Transformationen* -Parameters die instanztransformation ist, mit der der Produktcode geändert wird. Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**Methode "**](installer-advertiseproduct.md) ankündigen" verwendet die [**msiankündigen-productex**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) -Funktion.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der Methode " **kreatewerbung** " veranschaulicht.


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
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 4,5 unter Windows Server 2003 und Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Installationsprogramm**](installer-object.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




