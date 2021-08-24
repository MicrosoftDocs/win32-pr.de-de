---
description: Die SetAsSingleton-Methode des SWbemObjectPath-Objekts erzwingt, dass der Pfad eine Singleton-WMI-Instanz einer Klasse adressiert. Eine Singletonklasse ist eine Klasse, die nie mehr als eine Instanz haben darf.
ms.assetid: 7ec53954-2aac-494c-87c7-6a14592d8bd5
ms.tgt_platform: multiple
title: SWbemObjectPath.SetAsSingleton-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4a8a46566990021a4de4fca95b2b524cc7ddc1f5a797d7e3bffd0dc34ee52186
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568260"
---
# <a name="swbemobjectpathsetassingleton-method"></a>SWbemObjectPath.SetAsSingleton-Methode

Die **SetAsSingleton-Methode** des [**SWbemObjectPath-Objekts**](swbemobjectpath.md) erzwingt, dass der Pfad eine Singleton-WMI-Instanz einer Klasse adressiert. Eine Singletonklasse ist eine Klasse, die nie mehr als eine Instanz haben darf.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md) SWbemObjectPath

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.SetAsSingleton()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **SetAsSingleton-Methode** kann das **Err-Objekt** den folgenden Fehlercode enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



 

 




