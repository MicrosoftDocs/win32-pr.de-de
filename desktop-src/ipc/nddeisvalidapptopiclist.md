---
description: Bestimmt, ob eine Anwendung und eine Themenzeichenfolge (&\# 0034; AppName \| TopicName&\# 0034;) verwendet die richtige Syntax.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: NDdeIsValidAppTopicList-Funktion (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: f7b70d3e33f67c8c0a457f85df91e83e374a3ef4d0f0b1a0af1c5c41ea81c2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611130"
---
# <a name="nddeisvalidapptopiclist-function"></a>NDdeIsValidAppTopicList-Funktion

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NICHT \_ IMPLEMENTIERT zurück.\]

Bestimmt, ob eine Anwendungs- und Themenzeichenfolge ("*AppName* \| *TopicName*") die richtige Syntax verwendet.

## <a name="syntax"></a>Syntax


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*targetTopic* \[ In\]
</dt> <dd>

Ein Zeiger auf die zu überprüfende Anwendung und Themenzeichenfolge. Dieser Parameter darf nicht **NULL sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der *targetTopic-Parameter* über eine gültige Syntax verfügt, ist der Rückgabewert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

Diese Funktion wird auch von [**NDdeShareAdd aufgerufen,**](nddeshareadd.md) wenn die DDE-Freigabe erstellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                      |
| Header<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>      |
| Bibliothek<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl>    |
| Unicode- und ANSI-Name<br/>   | **NDdeIsValidAppTopicListW** (Unicode) und **NDdeIsValidAppTopicListA** (ANSI)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht dynamische Daten Exchange Netzwerksicherheit](network-dynamic-data-exchange.md)
</dt> <dt>

[DDE-Netzwerkfunktionen](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




