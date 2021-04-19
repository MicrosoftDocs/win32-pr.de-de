---
description: Die "Werbung"-Methode des Installerobjekts gibt ein Installationspaket an.
ms.assetid: 45e5268f-7a5f-412f-b9f6-0abb75b79361
title: 'Installer:: Werbung-Methode'
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
ms.openlocfilehash: 7e4ec5afae8d870511c6f91502f8b5844ce135bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366690"
---
# <a name="installeradvertisescript-method"></a>Installer:: Werbung-Methode

Die " **Werbung** "-Methode des [**Installerobjekts**](installer-object.md) gibt ein Installationspaket an.

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

Der vollständige Pfad zu der Skriptdatei, die von der Methode " [**kreatewerbung**](installer-createadvertisescript.md) " generiert wurde.

</dd> <dt>

*scriptflags* 
</dt> <dd>

Die Flags, die die Ankündigung steuern. Dieser Parameter kann eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseScriptCacheInfo"></span><span id="msiadvertisescriptcacheinfo"></span><span id="MSIADVERTISESCRIPTCACHEINFO"></span><dl> <dt>**msiwerbesescriptcacheingefo**</dt> <dt>0x001</dt> </dl>                                                                 | Fügen Sie dieses Flag ein, wenn die Symbole erstellt oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="msiAdvertiseScriptShortcuts"></span><span id="msiadvertisescriptshortcuts"></span><span id="MSIADVERTISESCRIPTSHORTCUTS"></span><dl> <dt>**msiwerbesescriptverknüpfungen**</dt> <dt>0x004</dt> </dl>                                                                 | Fügen Sie dieses Flag ein, wenn die Tastenkombinationen erstellt oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptMachineAssign"></span><span id="msiadvertisescriptmachineassign"></span><span id="MSIADVERTISESCRIPTMACHINEASSIGN"></span><dl> <dt>**msiwerbesescriptmachineassign**</dt> <dt>0x008</dt> </dl>                                                 | Fügen Sie dieses Flag ein, wenn das Produkt einem Computer zugewiesen werden soll.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptConfigurationRegistration"></span><span id="msiadvertisescriptconfigurationregistration"></span><span id="MSIADVERTISESCRIPTCONFIGURATIONREGISTRATION"></span><dl> <dt>**msiwerbesescriptconfigurationregistration**</dt> <dt>0x020</dt> </dl> | Fügen Sie dieses Flag ein, wenn die Konfigurations-und Verwaltungsinformationen in den Registrierungsdaten geschrieben oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptValidateTransformList"></span><span id="msiadvertisescriptvalidatetransformlist"></span><span id="MSIADVERTISESCRIPTVALIDATETRANSFORMLIST"></span><dl> <dt>**msiwerbesescriptvalidatetransformlist**</dt> <dt>0x040</dt> </dl>                 | Fügen Sie dieses Flag ein, um die Überprüfung der im Skript aufgelisteten Transformationen auf zuvor registrierte Transformationen für dieses Produkt zu erzwingen. Beachten Sie, dass Transformations Konflikte mithilfe eines Zeichen folgen Vergleichs erkannt werden, bei dem die Groß-und Kleinschreibung nicht beachtet wird und die zwischen den Installationen pro Benutzer und Computer übergreifend in allen [Installations Kontexten](installation-context.md)ausgewertet werden<br/> |
| <span id="msiAdvertiseScriptClassInfoRegistration"></span><span id="msiadvertisescriptclassinforegistration"></span><span id="MSIADVERTISESCRIPTCLASSINFOREGISTRATION"></span><dl> <dt>**msiwerbesescriptclassinforegistration**</dt> <dt>0x080</dt> </dl>                 | Fügen Sie dieses Flag ein, wenn Ankündigungs Informationen in der Registrierung in Bezug auf COM-Klassen geschrieben oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                    |
| <span id="msiAdvertiseScriptExtensionInfoRegistration"></span><span id="msiadvertisescriptextensioninforegistration"></span><span id="MSIADVERTISESCRIPTEXTENSIONINFOREGISTRATION"></span><dl> <dt>**msiwerbesescriptextensioninforegistration**</dt> <dt>0x100</dt> </dl> | Fügen Sie dieses Flag ein, wenn Ankündigungs Informationen in der mit einer Erweiterung verknüpften Registrierung geschrieben oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptAppInfo"></span><span id="msiadvertisescriptappinfo"></span><span id="MSIADVERTISESCRIPTAPPINFO"></span><dl> <dt>**msiwerbesescriptappinfo**</dt> <dt>0x180</dt> </dl>                                                                         | Fügen Sie dieses Flag ein, wenn die Ankündigungs Informationen in der Registrierung geschrieben oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                                       |
| <span id="msiAdvertiseScriptRegData"></span><span id="msiadvertisescriptregdata"></span><span id="MSIADVERTISESCRIPTREGDATA"></span><dl> <dt>**msiwerbesescriptregdata**</dt> <dt>0x1a0</dt> </dl>                                                                         | Fügen Sie dieses Flag ein, wenn die Ankündigungs Informationen in der Registrierung geschrieben oder entfernt werden müssen.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

*RemoveItems* 
</dt> <dd>

TRUE, wenn die angegebenen Elemente entfernt werden sollen, anstatt erstellt zu werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Methode " **Werbung** " verwendet die Funktion " [**msiwerbesescript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta) ". Die Verwendung der " **Werbung** "-Methode erfordert, dass das Skript in einem lokalen System Prozess ausgeführt wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der Methode " **Werbung** " veranschaulicht.


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
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 4,5 unter Windows Server 2003 und Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Installationsprogramm**](installer-object.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




