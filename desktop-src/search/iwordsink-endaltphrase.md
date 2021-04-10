---
description: Gibt das Ende des abschließenden Ausdrucks in einer Sequenz alternativer Ausdrücke an, die eine Wörter Trennung während der Index Zeit generiert.
ms.assetid: 50E4E208-A290-42B7-9152-9472C01B20D5
title: 'Iwordsink:: endaltphrase-Methode (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.EndAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 4056357de5e3e479124e8f9a91d9b3d906300709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214448"
---
# <a name="iwordsinkendaltphrase-method"></a>Iwordsink:: endaltphrase-Methode

Gibt das Ende des abschließenden Ausdrucks in einer Sequenz alternativer Ausdrücke an, die eine Wörter Trennung während der Index Zeit generiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndAltPhrase();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                           | Beschreibung                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**nur wbreak \_ E- \_ Abfrage \_**</dt> </dl> | [**Endaltphrase**](iwordsink-endaltphrase.md) wird während der Abfragezeit aufgerufen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

[**Iwordbreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) -Implementierungen wenden **iwordsink:: endaltphrase** von der [**iwordbreak:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) -Methode an, um eine Sequenz alternativer Ausdrücke zu beenden. Die [**iwordsink:: startaltphrase**](iwordsink-startaltphrase.md) -Methode wird aufgerufen, um das Ende eines Ausdrucks und den Anfang eines anderen in einer Sequenz von Ausdrücken anzugeben. Nur der letzte Ausdruck in einer Sequenz wird mit einem-Befehl von **endaltphrase** beendet.

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

 

 
