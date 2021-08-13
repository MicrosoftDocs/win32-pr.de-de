---
description: Die AdvertiseScript-Methode des Installer-Objekts kündigt ein Installationspaket an.
ms.assetid: 45e5268f-7a5f-412f-b9f6-0abb75b79361
title: Installer::AdvertiseScript-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f6a3ca8b4c07b4bd19b9f5d5066ed17dcc5aa7edb5828741e32ee05197a83777
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633217"
---
# <a name="installeradvertisescript-method"></a>Installer::AdvertiseScript-Methode

Die **AdvertiseScript-Methode** des [**Installer-Objekts**](installer-object.md) kündigt ein Installationspaket an.

## <a name="syntax"></a>Syntax


```JScript
.AdvertiseScript(
  scriptPath,
  scriptFlags,
  removeItems
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*scriptPath* 
</dt> <dd>

Der vollständige Pfad zur Skriptdatei, die von der [**CreateAdvertiseScript-Methode**](installer-createadvertisescript.md) generiert wurde.

</dd> <dt>

*scriptFlags* 
</dt> <dd>

Die Flags, die die Ankündigung steuern. Dieser Parameter kann eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseScriptCacheInfo"></span><span id="msiadvertisescriptcacheinfo"></span><span id="MSIADVERTISESCRIPTCACHEINFO"></span><dl> <dt>**msiAdvertiseScriptCacheInfo-0x001**</dt> <dt></dt> </dl>                                                                 | Schließen Sie dieses Flag ein, wenn die Symbole erstellt oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="msiAdvertiseScriptShortcuts"></span><span id="msiadvertisescriptshortcuts"></span><span id="MSIADVERTISESCRIPTSHORTCUTS"></span><dl> <dt>**msiAdvertiseScriptShortcuts**</dt> <dt>0x004</dt> </dl>                                                                 | Schließen Sie dieses Flag ein, wenn die Verknüpfungen erstellt oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptMachineAssign"></span><span id="msiadvertisescriptmachineassign"></span><span id="MSIADVERTISESCRIPTMACHINEASSIGN"></span><dl> <dt>**msiAdvertiseScriptMachineAssign**</dt> <dt>0x008</dt> </dl>                                                 | Schließen Sie dieses Flag ein, wenn das Produkt einem Computer zugewiesen werden soll.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptConfigurationRegistration"></span><span id="msiadvertisescriptconfigurationregistration"></span><span id="MSIADVERTISESCRIPTCONFIGURATIONREGISTRATION"></span><dl> <dt>**msiAdvertiseScriptConfigurationRegistration**</dt> <dt>0x020</dt> </dl> | Schließen Sie dieses Flag ein, wenn die Konfigurations- und Verwaltungsinformationen in den Registrierungsdaten geschrieben oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptValidateTransformList"></span><span id="msiadvertisescriptvalidatetransformlist"></span><span id="MSIADVERTISESCRIPTVALIDATETRANSFORMLIST"></span><dl> <dt>**msiAdvertiseScriptValidateTransformList**</dt> <dt>0x040</dt> </dl>                 | Schließen Sie dieses Flag ein, um die Überprüfung der im Skript aufgeführten Transformationen für zuvor registrierte Transformationen für dieses Produkt zu erzwingen. Beachten Sie, dass Transformationskonflikte mithilfe eines Zeichenfolgenvergleichs erkannt werden, bei dem die Groß-/Kleinschreibung nicht beachtet wird und der zwischen benutzer- und computerbezogenen Installationen in allen [Installationskontexten](installation-context.md)ausgewertet wird.<br/> |
| <span id="msiAdvertiseScriptClassInfoRegistration"></span><span id="msiadvertisescriptclassinforegistration"></span><span id="MSIADVERTISESCRIPTCLASSINFOREGISTRATION"></span><dl> <dt>**msiAdvertiseScriptClassInfoRegistration**</dt> <dt>0x080</dt> </dl>                 | Schließen Sie dieses Flag ein, wenn Ankündigungsinformationen in der Registrierung im Zusammenhang mit COM-Klassen geschrieben oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                    |
| <span id="msiAdvertiseScriptExtensionInfoRegistration"></span><span id="msiadvertisescriptextensioninforegistration"></span><span id="MSIADVERTISESCRIPTEXTENSIONINFOREGISTRATION"></span><dl> <dt>**msiAdvertiseScriptExtensionInfoRegistration**</dt> <dt>0x100</dt> </dl> | Schließen Sie dieses Flag ein, wenn Ankündigungsinformationen in der Registrierung, die sich auf eine Erweiterung beziehen, geschrieben oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptAppInfo"></span><span id="msiadvertisescriptappinfo"></span><span id="MSIADVERTISESCRIPTAPPINFO"></span><dl> <dt>**msiAdvertiseScriptAppInfo**</dt> <dt>0x180</dt> </dl>                                                                         | Schließen Sie dieses Flag ein, wenn die Ankündigungsinformationen in der Registrierung geschrieben oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                                       |
| <span id="msiAdvertiseScriptRegData"></span><span id="msiadvertisescriptregdata"></span><span id="MSIADVERTISESCRIPTREGDATA"></span><dl> <dt>**msiAdvertiseScriptRegData-0x1A0**</dt> <dt></dt> </dl>                                                                         | Schließen Sie dieses Flag ein, wenn die Ankündigungsinformationen in der Registrierung geschrieben oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

*removeItems* 
</dt> <dd>

TRUE, wenn die angegebenen Elemente entfernt werden sollen, anstatt erstellt zu werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **AdvertiseScript-Methode** verwendet die [**MsiAdvertiseScript-Funktion.**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta) Die Verwendung der **AdvertiseScript-Methode** erfordert, dass das Skript in einem lokalen Systemprozess ausgeführt wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **AdvertiseScript-Methode** veranschaulicht.


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' Advertise Simple package using an advertise script
'   created by CreateAdvertiseScript Method
'
'  Flags 424 indicate msiAdvertiseScriptMachineAssign, msiAdvertiseScriptRegData

Installer.AdvertiseScript "c:\scratch\simpletst\rtm\simple.aas", 424, false

' Verify Simple is installed
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")

'
' Remove Simple using advertise script
'
Installer.AdvertiseScript "c:\scratch\simpletst\rtm\simple.aas", 424, true

' Verify simple is removed
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 4.5 auf Windows Server 2003 und Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Installer**](installer-object.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 3.1 und früheren Versionen](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




