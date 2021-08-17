---
description: Die Add-Methode des SWbemPrivilegeSet-Objekts fügt der SWbemPrivilegeSet-Sammlung ein SWbemPrivilege-Objekt hinzu. Wenn bereits eine Berechtigung mit dem gleichen Namen in der Auflistung vorhanden ist, wird sie ersetzt.
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: SWbemPrivilegeSet.Add-Methode (Wbemdisp.h)
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
ms.openlocfilehash: 54b45779f4954f1cee454b5cf171e374e215555902e3389c7c47f5a59bc989eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954870"
---
# <a name="swbemprivilegesetadd-method"></a>SWbemPrivilegeSet.Add-Methode

Die **Add-Methode** des [**SWbemPrivilegeSet-Objekts**](swbemprivilegeset.md) fügt der **SWbemPrivilegeSet-Sammlung ein SWbemPrivilege-Objekt** hinzu. [](swbemprivilege.md) Wenn bereits eine Berechtigung mit dem gleichen Namen in der Auflistung vorhanden ist, wird sie ersetzt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iPrivilege* 
</dt> <dd>

Erforderlich. Eine der WMI-Konstanten aus der [**Gruppe WbemPrivilegeEnum.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) Diese Konstanten sind im Wesentlichen ganze Zahlen, die bestimmte Berechtigungen darstellen. Um beispielsweise die Berechtigung hinzuzufügen, mit der Sie ein Computersystem herunterfahren können, verwenden Sie die **Konstante wbemPrivilegeShutdown.** In einem Skript müssen Sie die numerische Entsprechung von 23 (0x17. Eine vollständige Liste dieser Konstanten und der zugeordneten Berechtigungszeichenfolgen finden Sie unter [**Privilege Constants**](privilege-constants.md).

</dd> <dt>

*bIsEnabled* \[ Optional\]
</dt> <dd>

Boolescher Wert, der diese Berechtigung aktiviert oder deaktiviert. Der Standardwert ist **TRUE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt die Methode ein [**SWbemPrivilege-Objekt**](swbemprivilege.md) zurück, das die neue Berechtigung darstellt. Andernfalls wird ein NULL-Objekt zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Add-Methode** kann das **Err-Objekt** den Fehlercode in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> </dl>

## <a name="examples"></a>Beispiele

Ein Codebeispiel mit dieser Methode wird im [**Thema SWbemPrivilegeSet**](swbemprivilegeset.md) beschrieben.

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

[Ausführen privilegierter Vorgänge mit VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md)
</dt> <dt>

[**SWbemPrivilegeSet.Remove**](swbemprivilegeset-remove.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Berechtigungskonst constants**](privilege-constants.md)
</dt> </dl>

 

 




