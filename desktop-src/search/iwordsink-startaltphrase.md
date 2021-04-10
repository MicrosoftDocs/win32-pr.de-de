---
description: Gibt die Begrenzung zwischen Ausdrücken in einer Sequenz alternativer Ausdrücke an, die eine Wörter Trennung während der Index Zeit generiert.
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: 'Iwordsink:: startaltphrase-Methode (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.StartAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e4e35c5ed75016292dd420e7a832c6cfb780284a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214447"
---
# <a name="iwordsinkstartaltphrase-method"></a>Iwordsink:: startaltphrase-Methode

Gibt die Begrenzung zwischen Ausdrücken in einer Sequenz alternativer Ausdrücke an, die eine Wörter Trennung während der Index Zeit generiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT StartAltPhrase();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                           | Beschreibung                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**nur wbreak \_ E- \_ Abfrage \_**</dt> </dl> | [**Startaltphrase**](iwordsink-startaltphrase.md) wird während der Abfragezeit aufgerufen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Jeder Alternative Ausdruck beginnt mit einem **startaltphrase** -Befehl. Der Ausdruck wird durch nachfolgende Aufrufe der [**iwordsink::P utword**](iwordsink-putword.md) -Methode oder der [**iwordsink::P utaltword**](iwordsink-putaltword.md) -Methode in das [**iwordsink**](iwordsink.md) -Objekt eingefügt. Der endgültige Alternative Ausdruck in einer Sequenz von Ausdrücken wird mit einem-Rückruf der [**iwordsink:: endaltphrase**](iwordsink-endaltphrase.md) -Methode beendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Search. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwordsink**](iwordsink.md)
</dt> </dl>

 

 




