---
description: Verwenden Sie zum Erstellen einer neuen Instanz einer-Klasse die SpawnInstance- \_ Methode des errbemubject-Objekts.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: SWbemObject.SpawnInstance_-Methode (wbemdisp. h)
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
ms.openlocfilehash: 804c7d2828723ee8da5dae28321faab62a32a0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218300"
---
# <a name="swbemobjectspawninstance_-method"></a>Errbemubject. SpawnInstance- \_ Methode

Verwenden Sie zum Erstellen einer neuen Instanz einer-Klasse die **SpawnInstance \_** -Methode des [**errbemubject**](swbemobject.md) -Objekts. Das aktuelle-Objekt muss eine Klassendefinition sein, die von WMI über eine Methode wie z. b. " [**Swap Services. Get**](swbemservices-get.md) " oder [**SWbemServices.Execquery**](swbemservices-execquery.md)abgerufen wird. Verwenden Sie dann diese Klassendefinition, um neue Instanzen zu erstellen. Erstellen Sie jede neue Instanz lokal innerhalb des Prozesses, und rufen Sie dann " [**errbemubject. Put \_**](swbemobject-put-.md) " auf, um die Instanz in WMI tatsächlich zu erstellen.

> [!Note]  
> Das Erzeugen einer Instanz aus einer-Instanz wird unterstützt, aber die zurückgegebene-Instanz ist leer.

 

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reserviert und muss NULL sein, wenn angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, gibt dieser-Befehl ein " [**errbemujebject**](swbemobject.md) "-Objekt mit einer neuen Instanz der-Klasse zurück.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **SpawnInstance \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

Das aktuelle Objekt ist keine gültige Klassendefinition, und es kann keine neuen Instanzen erzeugen. Entweder ist sie unvollständig, oder Sie wurde nicht bei WMI mithilfe von " [**errbemubject. Put \_**](swbemobject-put-.md)" registriert.

</dd> <dt>

**wbemErrIllegalOperation** -2147749918 (0x8004101e)
</dt> <dd>

Wird zurückgegeben, wenn diese Methode für eine-Instanz anstelle einer-Klasse verwendet wird.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch Objekt<br/>                                                           |
| IID<br/>                      | IID \_ iswbemujekt<br/>                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Austausch Objekt**](swbemobject.md)
</dt> <dt>

[**Swap-Datei\_**](swbemobject-put-.md)
</dt> <dt>

[**Austauschdienste. Get**](swbemservices-get.md)
</dt> </dl>

 

 




