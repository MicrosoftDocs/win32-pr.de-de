---
description: Die ProvideAssembly-Methode des Installer-Objekts gibt den installierten Pfad einer Assembly zurück.
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: Installer::P rovideAssembly-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 45d5c2d6b64936b034d859caddf72ddaaf6fba77451d066205d7f394200311f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105210"
---
# <a name="installerprovideassembly-method"></a>Installer::P rovideAssembly-Methode

Die **ProvideAssembly-Methode** des [**Installer-Objekts**](installer-object.md) gibt den installierten Pfad einer Assembly zurück.

## <a name="syntax"></a>Syntax


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Versammlung* 
</dt> <dd>

Der starke Name der installierten Assembly, die abgefragt werden soll.

</dd> <dt>

*appContext* 
</dt> <dd>

Legen Sie für globale Assemblys auf NULL fest. Legen Sie *appContext* für private Assemblys auf den vollständigen Pfad der Anwendungskonfigurationsdatei oder auf den vollständigen Pfad der ausführbaren Datei der Anwendung fest, für die die Assembly als privat festgelegt wurde.

</dd> <dt>

*installMode* 
</dt> <dd>

Definiert den Installationsmodus. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                                | Stellen Sie die Komponente bereit, und führen Sie alle installationen aus, die für die Bereitstellung der Komponente erforderlich sind. <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>-1</dt> </dl>                                                                                           | Geben Sie die Komponente nur an, wenn das Feature vorhanden ist. Mit dieser Option wird überprüft, ob die Assembly vorhanden ist.<br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt> </dl>                                                                               | Geben Sie die Komponente nur an, wenn das Feature vorhanden ist. Mit dieser Option wird nicht überprüft, ob die Assembly vorhanden ist.<br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt> </dl>                                                   | Stellt die Assembly nur bereit, wenn die Assembly lokal installiert ist.<br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <dt>**Kombination der von [ **ReinstallFeature** verwendeten Flags](installer-reinstallfeature.md)**</dt> </dl> | Ruft die [**ReinstallFeature-Methode**](installer-reinstallfeature.md) auf, um das Feature mit diesem Parameter für *ReinstallMode* neu zu installieren, und gibt dann den Assemblypfad zurück.<br/> |



 

</dd> <dt>

*Assemblyinfo* 
</dt> <dd>

Assemblyinformationen und Assemblytyp. Legen Sie auf einen der folgenden Werte fest.



| Wert                                                                                                                                                                                                                                                                                       | Bedeutung                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <dt>**msiProvideAssemblyNet**</dt> <dt>0</dt> </dl>         | Eine .NET-Assembly.<br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt> </dl> | Eine win32-seitige Assembly.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Pfad zur installierten Assembly.

## <a name="remarks"></a>Hinweise

Die **ProvideAssembly-Methode** verwendet die [**MsiProvideAssembly-Funktion.**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)

## <a name="examples"></a>Beispiele

Das folgende Beispielskript veranschaulicht die Verwendung der ProvideAssembly-Methode.


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 4.5 auf Windows Server 2003 und Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Installer**](installer-object.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 3.1 und früheren Versionen](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




