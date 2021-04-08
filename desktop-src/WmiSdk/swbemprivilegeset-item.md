---
description: Die Item-Methode des-Objekts von "taubemprivilegeset" gibt ein-Objekt aus der-Auflistung zurück. Die Item-Methode ist die Standardmethode eines "taubemprivilegeset"-Objekts.
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: Taubemprivilegeset. Item-Methode (wbemdisp. h)
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
ms.openlocfilehash: 7ea37ae758ec599198fc35a1fd2a4b89ff25a087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863767"
---
# <a name="swbemprivilegesetitem-method"></a>Taubemprivilegeset. Item-Methode

Die **Item** -Methode des-Objekts von " [**taubemprivilegeset**](swbemprivilegeset.md) " [**gibt ein-**](swbemprivilege.md) Objekt aus der-Auflistung zurück. Die **Item** -Methode ist die Standardmethode eines " **taubemprivilegeset** "-Objekts.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iprivilege* 
</dt> <dd>

Erforderlich. Eine der WMI-Konstanten aus der [**wbemprivilegeenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) -Gruppe. Diese Konstanten sind im wesentlichen ganze Zahlen, die bestimmte Berechtigungen darstellen. Um z. b. die Berechtigung zu erhalten, mit der Sie ein Windows-System Herunterfahren können, verwenden Sie die Konstante **wbemprivilegeshutdown** oder die numerische Entsprechung 23 (0x17).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung wird das angeforderte " [**taubemprivilege**](swbemprivilege.md) "-Objekt zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **Item** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Die angegebene Berechtigung ist nicht vorhanden.

</dd> </dl>

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird die **Item** -Methode verwendet.


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-taubemprivilegeset<br/>                                                     |
| IID<br/>                      | IID \_ iswbemprivilegeset<br/>                                                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swap-Privileg**](swbemprivilegeset.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge](executing-privileged-operations.md)
</dt> <dt>

[**Austausch Berechtigung**](swbemprivilege.md)
</dt> </dl>

 

 




