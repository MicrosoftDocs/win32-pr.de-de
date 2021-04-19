---
description: Legt den rights-Parameter als Bitmap fest, wobei jedes Bit einem Zugriffsrecht entspricht.
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: Getcalleraccessrights-Methode der __SystemSecurity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: c86ea3044411e33026ed6328fcfc227e615648b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353852"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a>Getcalleraccessrights-Methode der \_ \_ System Security-Klasse

Die **\_ \_ SystemSecurity:: getcalleraccessrights** -Methode legt den *Rights* -Parameter als Bitmap fest, wobei jedes Bit einem Zugriffsrecht entspricht. Jeder Client kann diesen Befehl zum Bestimmen der Rechte des Clients abrufen. Diese Methode ist nützlich für Clients, die Features aktivieren oder deaktivieren. Beispielsweise kann eine GUI-Anwendung eine Schaltfläche deaktivieren, wenn der aktuell angemeldete Benutzer nicht über Methoden Ausführungsrechte verfügt.

Jeder aktivierte Client hat das Recht, **getcalleraccessrights** aufzurufen, auch wenn dieser Client nicht über allgemeine Methoden Ausführungsrechte verfügt.

## <a name="syntax"></a>Syntax


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Rechte* \[ vorgenommen\]
</dt> <dd>

Zugriffsrechte des Clients. Weitere Informationen finden Sie unter [**\_ \_ SystemSecurity**](--systemsecurity.md) und [WMI-Sicherheits Konstanten](wmi-security-constants.md).

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ Aktivieren** (1 (0x1))


</dt> <dd>

Aktiviert das Konto und gewährt dem Benutzer Leseberechtigungen. Dies ist das Standard Zugriffsrecht für alle Benutzer.

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ Methode \_ Execute** (2 (0x2))


</dt> <dd>

Ermöglicht die Ausführung von-Methoden.

> [!Note]  
> Anbieter können zusätzliche Zugriffs Überprüfungen durchführen.

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ Vollständiger \_ Schreib \_** Zugriff (4 (0x4))


</dt> <dd>

Ermöglicht es dem Aufrufer, dem Sicherheitskontext oder dem Benutzer, in Klassen und Instanzen mit Ausnahme von System Klassen zu schreiben.

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ Partieller \_ Schreib \_ Rep** (8 (0x8))


</dt> <dd>

Ermöglicht dem Aufrufer, dem Sicherheitskontext oder dem Benutzer das Schreiben von Anbieter Instanzen, aber nicht von statischen Klassen oder statischen Instanzen in das Repository.

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ Schreib \_ Anbieter** (16 (0x10))


</dt> <dd>

Ermöglicht dem Aufrufer, dem Sicherheitskontext oder dem Benutzer das Schreiben von Klassen und Instanzen in Anbieter.

> [!Note]  
> Die Identitätswechsel von Anbietern können zusätzliche Zugriffs Überprüfungen durchführen.

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ Remote \_ Zugriff** (32 (0x20))


</dt> <dd>

Ermöglicht einem Benutzerkonto das Remote Ausführen von Vorgängen, die von den von anderen Bits festgelegten Berechtigungen zugelassen werden.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Lesen Sie \_ Steuer** Element (131072 (0x20000))


</dt> <dd>

Ermöglicht den Lesezugriff auf die Sicherheits Deskriptoren.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Schreiben \_ DAC** (262144 (0x40000))


</dt> <dd>

Ermöglicht den Schreibzugriff auf freigegebene Zugriffs Steuerungs Listen (DACL).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **HRESULT** zurück, das den Status des Methoden Aufrufes angibt. In der folgenden Liste sind die Rückgabewerte aufgelistet, die für [**Set9XUserList**](--systemsecurity-set9xuserlist.md)von Bedeutung sind. Für Skript-und Visual Basic Anwendungen kann das Ergebnis aus " [OutParameters. returnValue](parsing-outparameters-objects.md)" abgerufen werden. Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**WBEM \_ E- \_ Methode \_ deaktiviert**
</dt> <dd>

Diese Methode wird auf unterstützten Versionen von Windows nicht unterstützt.

</dd> </dl>

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

[**\_\_SystemSecurity:: getd**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity::-ID**](--systemsecurity-setsd.md)
</dt> <dt>

[WMI-Sicherheits Konstanten](wmi-security-constants.md)
</dt> <dt>

[**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Sichern von WMI-Namespaces](securing-wmi-namespaces.md)
</dt> <dt>

WMI-Sicherheits Konstanten
</dt> </dl>

 

