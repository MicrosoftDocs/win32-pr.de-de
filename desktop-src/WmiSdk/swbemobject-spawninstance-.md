---
description: Verwenden Sie die SpawnInstance-Methode \_ des SWbemObject-Objekts, um eine neue Instanz einer Klasse zu erstellen.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: SWbemObject.SpawnInstance_ -Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1b465bb53fd031dff397ef0ddf39db39d5d9987f03e037becebcd8dd41a65b87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640040"
---
# <a name="swbemobjectspawninstance_-method"></a>SWbemObject.SpawnInstance-Methode \_

Verwenden Sie **die SpawnInstance-Methode \_** des [**SWbemObject-Objekts,**](swbemobject.md) um eine neue Instanz einer Klasse zu erstellen. Das aktuelle Objekt muss eine Klassendefinition sein, die von WMI über eine Methode wie [**SWbemServices.Get**](swbemservices-get.md) oder cQuerySWbemServices.Exe [**wird.**](swbemservices-execquery.md) Verwenden Sie dann diese Klassendefinition, um neue Instanzen zu erstellen. Erstellen Sie jede neue Instanz lokal innerhalb des Prozesses, und rufen Sie [**dann SWbemObject.Put \_**](swbemobject-put-.md) auf, um die Instanz tatsächlich in WMI zu erstellen.

> [!Note]  
> Das Erstellen einer Instanz aus einer -Instanz wird unterstützt, aber die zurückgegebene Instanz ist leer.

 

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Reserviert und muss 0 (null) sein, wenn angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt dieser Aufruf ein [**SWbemObject-Objekt**](swbemobject.md) zurück, das eine neue Instanz der -Klasse enthält.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **\_ SpawnInstance-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrIncompleteClass** – 2147749920 (0x80041020)
</dt> <dd>

Das aktuelle Objekt ist keine gültige Klassendefinition und kann keine neuen Instanzen erstellen. Entweder ist sie unvollständig, oder sie wurde nicht mithilfe von [**SWbemObject.Put \_**](swbemobject-put-.md)bei WMI registriert.

</dd> <dt>

**wbemErrIllegalOperation** – 2147749918 (0x8004101E)
</dt> <dd>

Wird zurückgegeben, wenn diese Methode für eine -Instanz anstelle einer -Klasse verwendet wird.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Ungültiger Parameter wurde angegeben.

</dd> <dt>

**wbemErrOutOfMemory** : 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher zum Abschließen des Vorgangs.

</dd> </dl>

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swbemobject**](swbemobject.md)
</dt> <dt>

[**SWbemObject.Put\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServices.Get**](swbemservices-get.md)
</dt> </dl>

 

 




