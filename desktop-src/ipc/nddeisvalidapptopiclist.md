---
description: Bestimmt, ob eine Anwendung und eine Themen Zeichenfolge (&\# 0034; AppName \| TopicName&\# 0034;) verwendet die richtige Syntax.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: Nddeisvalidapptopiclist-Funktion (nddeapi. h)
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
ms.openlocfilehash: fb990830583f6684502438f132c1c98f5741a0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362665"
---
# <a name="nddeisvalidapptopiclist-function"></a>Nddeisvalidapptopiclist-Funktion

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Bestimmt, ob eine Anwendung und eine Themen Zeichenfolge ("*appname* \| *TopicName*") die richtige Syntax verwendet.

## <a name="syntax"></a>Syntax


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*targettopisch* \[ in\]
</dt> <dd>

Ein Zeiger auf die zu validierende Anwendungs-und Themen Zeichenfolge. Dieser Parameter darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der *targettopparameter* über eine gültige Syntax verfügt, ist der Rückgabewert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird auch von [**ndabshareadd**](nddeshareadd.md) aufgerufen, wenn Sie die DDE-Freigabe erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                      |
| Header<br/>                   | <dl> <dt>Ndde API. h</dt> </dl>      |
| Bibliothek<br/>                  | <dl> <dt>Ndde API. lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl>    |
| Unicode- und ANSI-Name<br/>   | **Nddeisvalidapptopiclistw** (Unicode) und **nddeisvalidapptopiclista** (ANSI)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Network DDE-Funktionen](network-dde-functions.md)
</dt> <dt>

[**Ndabshareadd**](nddeshareadd.md)
</dt> </dl>

 

 




