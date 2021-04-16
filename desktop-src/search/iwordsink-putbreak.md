---
description: Versetzt nach dem vorangehenden Wort einen Umbruch.
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: Iwordsink::P utbreak-Methode (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutBreak
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: c6407f1307b4860960c5202af13de736c7921139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342929"
---
# <a name="iwordsinkputbreak-method"></a>Iwordsink::P utbreak-Methode

Versetzt nach dem vorangehenden Wort einen Umbruch.

## <a name="syntax"></a>Syntax


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*breaktyp* \[ in\]
</dt> <dd>

Ein Wert aus dem [**wordrep- \_ \_ unterbruchtyp**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) , der den Typ der Unterbrechung angibt, den die wordsink nach dem vorangehenden Wort einfügt. Jede Unterbrechung nimmt eine eindeutige Position im Index auf. Daher wird durch Einfügen von Unterbrechungen zwischen Wörtern der relative Abstand zwischen Wörtern geändert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Der Vorgang wurde erfolgreich abgeschlossen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Methoden [**iwordsink putword**](iwordsink-putword.md) und [**iwordsink::P utaltword**](iwordsink-putaltword.md) fügen automatisch einen Ende der Wort Umbruch (EOW, der durch das wordrep \_ break \_ EOW-Element des Enumerationstyps der [**wordrep \_ \_**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) -Enumeration gekennzeichnet ist) nach jedem Wort ein. Ruft die **putbreak** -Methode auf, um einen anderen Bruchtyp als das Wort Ende einzufügen. Diese Methode ändert nicht den Quell Text Puffer (*psourcetext*) oder erhöht die Zeichen Anzahl (*CWC*). Allerdings wird die aktuelle Position im Index erhöht und wirkt sich auf die Abfrageergebnisse aus.

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

 

 
