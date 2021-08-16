---
description: Die Item-Methode des SWbemPrivilegeSet-Objekts gibt ein SWbemPrivilege-Objekt aus der Auflistung zurück. Die Item-Methode ist die Standardmethode eines SWbemPrivilegeSet-Objekts.
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: SWbemPrivilegeSet.Item-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 93180f168820acce2bf2564ef108c509713a22e68cfa16fbb8f2abeff17b5bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313522"
---
# <a name="swbemprivilegesetitem-method"></a>SWbemPrivilegeSet.Item-Methode

Die **Item-Methode** des [**SWbemPrivilegeSet-Objekts**](swbemprivilegeset.md) gibt ein [**SWbemPrivilege-Objekt**](swbemprivilege.md) aus der Auflistung zurück. Die **Item-Methode** ist die Standardmethode eines **SWbemPrivilegeSet-Objekts.**

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iPrivilege* 
</dt> <dd>

Erforderlich. Eine der WMI-Konstanten aus der [**Gruppe WbemPrivilegeEnum.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) Diese Konstanten sind im Wesentlichen ganze Zahlen, die bestimmte Berechtigungen darstellen. Um beispielsweise die Berechtigung zu erhalten, mit der Sie ein Windows-System herunterfahren können, verwenden Sie die **wbemPrivilegeShutdown-Konstante** oder die numerische Entsprechung 23 (0x17).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird das angeforderte [**SWbemPrivilege-Objekt**](swbemprivilege.md) zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Item-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Die angegebene Berechtigung ist nicht vorhanden.

</dd> </dl>

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird die **Item-Methode** verwendet.


```VB
strComputer ="."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")
Set colServices = objWMIService.ExecQuery( _
    "Select * from Win32_Service")
For Each objService In colServices
    WScript.Echo objService.Properties_.Item("Caption")
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge](executing-privileged-operations.md)
</dt> <dt>

[**SWbemPrivilege**](swbemprivilege.md)
</dt> </dl>

 

 




