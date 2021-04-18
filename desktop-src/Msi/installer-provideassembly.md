---
description: Die ProvideAssembly-Methode des Installer-Objekts gibt den installierten Pfad einer Assembly zurück.
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: Installer::P rovideassembly-Methode
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
ms.openlocfilehash: f81c9ab9b43b814307242cc828326b2b7e7d79fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371300"
---
# <a name="installerprovideassembly-method"></a>Installer::P rovideassembly-Methode

Die **ProvideAssembly** -Methode des [**Installer**](installer-object.md) -Objekts gibt den installierten Pfad einer Assembly zurück.

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

*Stadtverordneten* 
</dt> <dd>

Der starke Name der installierten Assembly, die abgefragt werden soll.

</dd> <dt>

*appContext* 
</dt> <dd>

Legen Sie für globale Assemblys auf NULL fest. Legen Sie für private Assemblys *appContext* auf den vollständigen Pfad der Anwendungs Konfigurationsdatei oder auf den vollständigen Pfad der ausführbaren Datei der Anwendung fest, in der die Assembly als privat erstellt wurde.

</dd> <dt>

*' installmode '* 
</dt> <dd>

Definiert den Installationsmodus. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiinstallmodedefault**</dt> <dt>0</dt> </dl>                                                                                                | Geben Sie die Komponente an, und führen Sie jede erforderliche Installation aus, um die Komponente bereitzustellen <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiinstallmodevorhandenes**</dt> <dt>-1</dt> </dl>                                                                                           | Geben Sie die Komponente nur dann an, wenn das Feature vorhanden ist. Mit dieser Option wird überprüft, ob die Assembly vorhanden ist.<br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiinstallmudenoerkennungs**</dt> <dt>-2</dt> </dl>                                                                               | Geben Sie die Komponente nur dann an, wenn das Feature vorhanden ist. Mit dieser Option wird nicht überprüft, ob die Assembly vorhanden ist.<br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiinstallmudenosourceresolution**</dt> <dt>-3</dt> </dl>                                                   | Stellt die Assembly nur dann bereit, wenn die Assembly lokal installiert ist.<br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <dt>**Kombination der von [ **reinstallfeature** verwendeten Flags](installer-reinstallfeature.md)**</dt> </dl> | Ruft die [**reinstallfeature**](installer-reinstallfeature.md) -Methode auf, um die Funktion mithilfe dieses Parameters für den *REINSTALLMODE* erneut zu installieren, und gibt dann den Assemblypfad zurück.<br/> |



 

</dd> <dt>

*assemblyInfo* 
</dt> <dd>

Assemblyinformationen und Assemblytyp. Legen Sie auf einen der folgenden Werte fest.



| Wert                                                                                                                                                                                                                                                                                       | Bedeutung                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <dt>**msiprovide assemblynet**</dt> <dt>0</dt> </dl>         | Eine .NET-Assembly.<br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt> </dl> | Eine parallele Win32-Assembly.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Pfad zur installierten Assembly.

## <a name="remarks"></a>Bemerkungen

Die **ProvideAssembly** -Methode verwendet die [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) -Funktion.

## <a name="examples"></a>Beispiele

Im folgenden Beispielskript wird die Verwendung der ProvideAssembly-Methode veranschaulicht.


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
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 4,5 unter Windows Server 2003 und Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Installationsprogramm**](installer-object.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




