---
description: Verwenden Sie die spawnderivedclass- \_ Methode des errbemubject-Objekts, um ein abgeleitetes Klassenobjekt aus dem aktuellen-Objekt zu erstellen. Das-Objekt muss eine Klassendefinition sein, die zur übergeordneten Klasse des erzeugten Objekts wird.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: SWbemObject.SpawnDerivedClass_-Methode (wbemdisp. h)
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
ms.openlocfilehash: 2b26e1d894e5ccc0d0fcec9d7ac9ad0101d18c7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215320"
---
# <a name="swbemobjectspawnderivedclass_-method"></a>Errbemubject. spawnderivedclass- \_ Methode

Verwenden Sie die **spawnderivedclass \_** -Methode des [**errbemubject**](swbemobject.md) -Objekts, um ein abgeleitetes Klassenobjekt aus dem aktuellen-Objekt zu erstellen. Das-Objekt muss eine Klassendefinition sein, die zur übergeordneten Klasse des erzeugten Objekts wird.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Reserviert und muss 0 (null) sein, wenn angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der-Befehl erfolgreich ausgeführt wurde, enthält das " [**errbemubject**](swbemobject.md) "-Objekt das neue Klassen Definitions Objekt. Wenn ein Fehler auftritt, wird kein Objekt zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **spawnderivedclass \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrIllegalOperation** -2147749918 (0x8004101e)
</dt> <dd>

Der Benutzer hat einen ungültigen Vorgang angefordert, z. b. das Abrufen einer Klasse aus einer Instanz.

</dd> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

Die Quell Klasse wurde nicht vollständig definiert oder bei WMI registriert, sodass eine neue abgeleitete Klasse nicht zulässig ist.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das zurückgegebene Objekt wird automatisch zu einer Unterklasse des aktuellen-Objekts. Dieses Verhalten kann nicht überschrieben werden. Es gibt keine andere Methode, mit der abgeleitete Klassen erstellt werden können.

Eine abgeleitete Klasse kann nicht von einer Klasse erstellt werden, die für Ihren eigenen Client Prozess lokal ist. Bevor Sie diese Methode zum Erstellen einer abgeleiteten Klasse verwenden, müssen Sie die Basisklasse erstellen. Rufen Sie zum Erstellen der Basisklasse die Datei " [**errbemubject. Put \_**](swbemobject-put-.md)" auf, und rufen Sie die Basisklasse mithilfe von " [**Swap Services. Get**](swbemservices-get.md)" ab.

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



 

 




