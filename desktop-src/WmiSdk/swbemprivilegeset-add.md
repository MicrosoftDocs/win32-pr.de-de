---
description: Durch die Add-Methode des Objekts "Swap-Objekt" wird der "Swap-Auflistung"-Auflistung ein "taubemprivilege"-Objekt hinzugefügt. Wenn eine Berechtigung mit dem gleichen Namen bereits in der Sammlung vorhanden ist, wird Sie ersetzt.
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: Taubemprivilegeset. Add-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 080b9d3e3ab6dbfc0ed8afc8ac0476981b7c26e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041999"
---
# <a name="swbemprivilegesetadd-method"></a>Taubemprivilegeset. Add-Methode

Durch die **Add** -Methode des Objekts " [**Swap**](swbemprivilegeset.md) -Objekt" wird der " **Swap** -Auflistung"-Auflistung ein " [**taubemprivilege**](swbemprivilege.md) "-Objekt hinzugefügt. Wenn eine Berechtigung mit dem gleichen Namen bereits in der Sammlung vorhanden ist, wird Sie ersetzt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iprivilege* 
</dt> <dd>

Erforderlich. Eine der WMI-Konstanten aus der [**wbemprivilegeenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) -Gruppe. Diese Konstanten sind im wesentlichen ganze Zahlen, die bestimmte Berechtigungen darstellen. Wenn Sie z. b. die Berechtigung hinzufügen möchten, mit der Sie ein Computersystem Herunterfahren können, verwenden Sie die Konstante **wbemprivilegeshutdown** . In einem Skript müssen Sie die numerische Entsprechung von 23 (0x17) verwenden. Eine umfassende Liste dieser Konstanten und der zugehörigen Berechtigungs Zeichenfolgen finden Sie unter [**Berechtigungs Konstanten**](privilege-constants.md).

</dd> <dt>

*bisenabled* \[ optionale\]
</dt> <dd>

Boolescher Wert, der dieses Privileg aktiviert oder deaktiviert. Der Standardwert ist " **true**".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung gibt die Methode ein-Objekt zurück, das die [**neue Berechtigung darstellt**](swbemprivilege.md) . Andernfalls wird ein NULL-Objekt zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Add** -Methode kann das **Err** -Objekt den Fehlercode in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> </dl>

## <a name="examples"></a>Beispiele

Ein Codebeispiel, in dem diese Methode verwendet wird, wird im Thema " [**chanbemprivilegeset**](swbemprivilegeset.md) " beschrieben.

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

[Ausführen privilegierter Vorgänge mit VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[**"Taubemprivilegeset. addasstring"**](swbemprivilegeset-addasstring.md)
</dt> <dt>

[**"Swap-privilegeset. Remove"**](swbemprivilegeset-remove.md)
</dt> <dt>

[**Wbemprivilegeumum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Berechtigungs Konstanten**](privilege-constants.md)
</dt> </dl>

 

 




