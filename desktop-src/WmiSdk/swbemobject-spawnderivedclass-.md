---
description: Verwenden Sie die SpawnDerivedClass-Methode des SWbemObject-Objekts, um ein abgeleitetes Klassenobjekt aus \_ dem aktuellen -Objekt zu erstellen. Das -Objekt muss eine Klassendefinition sein, die zur übergeordneten Klasse des erstellten Objekts wird.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: SWbemObject.SpawnDerivedClass_ -Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0ed0a01926c76ecfc4d393a4de8225d7d0c98a9904f113aed18cd1cb5f8ccabb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313794"
---
# <a name="swbemobjectspawnderivedclass_-method"></a>SWbemObject.SpawnDerivedClass-Methode \_

Verwenden Sie **die SpawnDerivedClass-Methode \_** des [**SWbemObject-Objekts,**](swbemobject.md) um ein abgeleitetes Klassenobjekt aus dem aktuellen -Objekt zu erstellen. Das -Objekt muss eine Klassendefinition sein, die zur übergeordneten Klasse des erstellten Objekts wird.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iFlags* \[ Optional\]
</dt> <dd>

Reserviert und muss 0 (null) sein, wenn angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Aufruf erfolgreich ist, enthält das [**SWbemObject-Objekt**](swbemobject.md) das neue Klassendefinitionsobjekt. Bei einem Fehler wird kein Objekt zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **\_ SpawnDerivedClass-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrIllegalOperation** – 2147749918 (0x8004101E)
</dt> <dd>

Der Benutzer hat einen unzulässigen Vorgang angefordert, z. B. das Erstellen einer Klasse aus einer -Instanz.

</dd> <dt>

**wbemErrIncompleteClass** – 2147749920 (0x80041020)
</dt> <dd>

Die Quellklasse wurde nicht vollständig definiert oder bei WMI registriert, sodass eine neue abgeleitete Klasse nicht zulässig ist.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher zum Abschließen des Vorgangs.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das zurückgegebene -Objekt wird automatisch zu einer Unterklasse des aktuellen -Objekts. Dieses Verhalten kann nicht überschrieben werden. Es gibt keine andere Methode, mit der Sie abgeleitete Klassen erstellen können.

Sie können keine abgeleitete Klasse aus einer Klasse erstellen, die lokal für Ihren eigenen Clientprozess ist. Bevor Sie diese Methode verwenden, um eine abgeleitete Klasse zu erstellen, müssen Sie die Basisklasse erstellen. Rufen Sie zum Erstellen der Basisklasse [**\_ SWbemObject.Put**](swbemobject-put-.md)auf, und rufen Sie die Basisklasse mithilfe von [**SWbemServices.Get ab.**](swbemservices-get.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




