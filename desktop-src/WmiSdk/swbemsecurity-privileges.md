---
description: Die Privileges-Eigenschaft ist ein Objekt vom Typ"taubemprivilegeset". Diese Eigenschaft wird verwendet, um bestimmte Windows-Berechtigungen zu aktivieren oder zu deaktivieren. Möglicherweise müssen Sie eine dieser Berechtigungen festlegen, um bestimmte Aufgaben mithilfe der Windows-Verwaltungsinstrumentation (WMI)-API auszuführen.
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: "' Swap Security. Privileges '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215309"
---
# <a name="swbemsecurityprivileges-property"></a>Swap Security. Privileges (Eigenschaft)

Die **Privileges** -Eigenschaft ist ein Objekt vom Typ" [**taubemprivilegeset**](swbemprivilegeset.md) ". Diese Eigenschaft wird verwendet, um bestimmte Windows-Berechtigungen zu aktivieren oder zu deaktivieren. Möglicherweise müssen Sie eine dieser Berechtigungen festlegen, um bestimmte Aufgaben mithilfe der Windows-Verwaltungsinstrumentation (WMI)-API auszuführen.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Diese Einstellung ermöglicht es Ihnen, Berechtigungen als Teil einer WMI-Monikerzeichenfolge zu erteilen oder aufzuheben. Eine umfassende Liste der anwendbaren Werte finden Sie unter [**wbemprivilegeenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) und [**Berechtigungs Konstanten**](privilege-constants.md).

Sie können die Berechtigungen für die Objekte " [**Swap Services**](swbemservices.md)", " [**errbewbject**](swbemobject.md)", " [**errbewbjectset**](swbemobjectset.md)", " [**errbewbjectpath**](swbemobjectpath.md)" und " [**taubemlocator**](swbemlocator.md) " ändern, indem Sie der Eigenschaft " **Privilegien** " [**die Objekte "**](swbemprivilege.md) ", ""

Es gibt wesentliche Unterschiede in der Art und Weise, in der verschiedene Versionen von Windows Änderungen an Berechtigungen behandeln. Wenn Sie eine Anwendung entwickeln, die nur auf Windows-Plattformen verwendet wird, können Sie Berechtigungen jederzeit festlegen oder widerrufen.

Im folgenden Beispiel wird die **SeDebugPrivilege-Berechtigung** für die anfängliche monikerverbindung festgelegt, [**um ein-**](swbemservices.md) Objekt zu erhalten.


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



Weitere Informationen zum Formatieren der Sicherheits Zeichenfolge für eine monikerverbindung finden Sie unter [**Berechtigungs Konstanten**](privilege-constants.md).

Im folgenden Beispiel wird dieselbe Aufgabe durchführt, die Berechtigung wird jedoch nach der anfänglichen Anmeldung bei WMI festgelegt.


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



Beachten Sie, dass Sie bei Aufrufen von " [**taubemprivilegeset. addasstring**](swbemprivilegeset-addasstring.md)" den vollständigen Namen der Sicherheits Berechtigung verwenden müssen, z. b. "Setter", anstelle von "Debug".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Sicherheit<br/>                                                         |
| IID<br/>                      | IID \_ iswbemsecurity<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Austausch Sicherheit**](swbemsecurity.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge](executing-privileged-operations.md)
</dt> <dt>

[**Swap-Privileg**](swbemprivilegeset.md)
</dt> </dl>

 

 




