---
description: Ruft die Sicherheits Beschreibung für den Namespace ab, mit dem der Benutzer verbunden ist. Diese Methode gibt eine Sicherheits Beschreibung im Format des binären Byte Arrays zurück. Wenn Sie ein Skript schreiben, verwenden Sie die getsecuritydescriptor-Methode.
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: Gezd-Methode der __SystemSecurity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d471db22a9f15a38ab693ae72332e5e1893b5c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360588"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a>Gezd-Methode der \_ \_ System Security-Klasse

Die **gezd-** Methode ruft die Sicherheits Beschreibung für den Namespace ab, mit dem der Benutzer verbunden ist. Diese Methode gibt eine Sicherheits Beschreibung im Format des binären Byte Arrays zurück. Wenn Sie ein Skript schreiben, verwenden Sie die [**getsecuritydescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) -Methode. Weitere Informationen finden Sie unter [Sichern von WMI-Namespaces](securing-wmi-namespaces.md) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).

Der Benutzer muss über die Berechtigung zum **Lesen von \_ Steuer** Elementen verfügen. Standardmäßig verfügen Administratoren über diese Berechtigung. Der einzige Teil der Sicherheits Beschreibung, die tatsächlich verwendet wird, ist die freigegebene Zugriffs Steuerungs Liste (DACL). Die DACL kann sowohl geerbte als auch nicht geerbte ACEs enthalten. Deny-und allow-ACEs sind zulässig.

Wenn Sie in C++ programmieren, können Sie den binären Sicherheits Deskriptor mithilfe von [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)und die Konvertierungs Methoden [**convertsecuritydescriptortostringsecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) und [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)bearbeiten.

## <a name="syntax"></a>Syntax


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SD* \[ vorgenommen\]
</dt> <dd>

Sicherheits Beschreibung im Format des binären Byte Arrays.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **HRESULT** zurück, das den Status des Methoden Aufrufes angibt. In der folgenden Liste sind die Rückgabewerte aufgelistet, die für **ge-d** von Bedeutung sind. Für Skript-und Visual Basic Anwendungen kann das Ergebnis aus " [OutParameters. returnValue](parsing-outparameters-objects.md)" abgerufen werden. Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**S \_ OK**
</dt> <dd>

Die Methode wurde erfolgreich ausgeführt.

</dd> <dt>

**WBEM \_ E- \_ Zugriff \_ verweigert**
</dt> <dd>

Der Aufrufer verfügt nicht über ausreichende Rechte, um diese Methode aufzurufen.

</dd> <dt>

**WBEM \_ E- \_ Methode \_ deaktiviert**
</dt> <dd>

Es wurde versucht, diese Methode auf einem nicht unterstützten System auszuführen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zum programmgesteuerten oder manuellen Ändern der Namespace Sicherheit finden Sie unter [Sichern von WMI-Namespaces](securing-wmi-namespaces.md).

## <a name="examples"></a>Beispiele

Das folgende Skript zeigt, wie Sie **getd** verwenden, um die aktuelle Sicherheits Beschreibung für den root \\ Cimv2-Namespace abzurufen und in das Bytearray zu ändern, das in **displaysd** angezeigt wird.


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[WMI-Sicherheits Konstanten](wmi-security-constants.md)
</dt> <dt>

[**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_\_SystemSecurity::-ID**](--systemsecurity-setsd.md)
</dt> <dt>

[**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sichern von WMI-Namespaces](securing-wmi-namespaces.md)
</dt> </dl>

 

