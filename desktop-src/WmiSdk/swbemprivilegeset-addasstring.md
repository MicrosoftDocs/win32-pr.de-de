---
description: Mithilfe der addasstring-Methode des Objekts "taubemprivilegeset" können Sie einer "taubemprivilegeset"-Sammlung mithilfe einer Berechtigungs Zeichenfolge eine Berechtigung hinzufügen.
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: Methode ' Swap. addasstring ' (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b3a740141b14766080a09d01b36b5c0202351eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369852"
---
# <a name="swbemprivilegesetaddasstring-method"></a>Taubemprivilegeset. addasstring-Methode

Mithilfe der **addasstring** -Methode des Objekts " [**taubemprivilegeset**](swbemprivilegeset.md) " können Sie einer " **taubemprivilegeset** "-Sammlung mithilfe einer Berechtigungs Zeichenfolge eine Berechtigung hinzufügen. Verwenden Sie diese Methode, um eine Berechtigung hinzuzufügen oder um eine Berechtigung für " [**Swap Security**](swbemsecurity.md) "-Objekte zu aktivieren. Weitere Informationen finden [Sie unter Ausführen privilegierter Vorgänge mit VBScript](executing-privileged-operations-using-vbscript.md).

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*"Strauch Berechtigung"* 
</dt> <dd>

Erforderlich. Eine der Berechtigungs Zeichenfolgen. Eine umfassende Liste dieser Zeichen folgen und der zugehörigen WMI-Konstanten finden Sie unter [**Berechtigungs Konstanten**](privilege-constants.md). Jede Berechtigungs Zeichenfolge stellt eine bestimmte Berechtigung dar. Wenn Sie z. b. die Berechtigung hinzufügen möchten, mit der ein Computersystem heruntergefahren wird, verwenden Sie die Zeichenfolge **SeShutdownPrivilege** .

</dd> <dt>

*bisenabled* \[ optionale\]
</dt> <dd>

Boolescher Wert, der dieses Privileg aktiviert oder deaktiviert. Der Standardwert ist **True**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, gibt diese Methode ein-Objekt zurück, das die [**neue Berechtigung darstellt**](swbemprivilege.md) . Andernfalls wird ein NULL-Objekt zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **addasstring** -Methode kann das **Err** -Objekt den Fehlercode in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> </dl>

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird ein neuer Port für einen Druckserver mit [**Win32 \_ tcpipprinterport**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport)erstellt. Für diesen Vorgang ist die **SeLoadDriverPrivilege-Berechtigung** erforderlich. Siehe [Ausführen privilegierter Vorgänge](executing-privileged-operations.md).


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



Ein Codebeispiel, in dem diese Methode verwendet wird, wird auch im Thema " [**chanbemprivilegeset**](swbemprivilegeset.md) " beschrieben.

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

[**Austauschen von "taubemprivilegeset. Add"**](swbemprivilegeset-add.md)
</dt> <dt>

[**"Swap-privilegeset. Remove"**](swbemprivilegeset-remove.md)
</dt> <dt>

[**Wbemprivilegeumum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Berechtigungs Konstanten**](privilege-constants.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge](executing-privileged-operations.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge mit VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

