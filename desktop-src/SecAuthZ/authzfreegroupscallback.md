---
description: Eine anwendungsdefinierte Funktion, die speicherbenutzerdefinierter Speicher frei gibt, der von der Funktion "HzComputeGroupsCallback" zugeordnet wird. HzFreeGroupsCallback ist ein Platzhalter für den anwendungsdefinierten Funktionsnamen.
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: Rückruffunktion "HzFreeGroupsCallback"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3cce78e261892fede79fb8fc76bc5b0d009342db3e0bf672be2854cb8492bcec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783764"
---
# <a name="authzfreegroupscallback-callback-function"></a>Rückruffunktion "HzFreeGroupsCallback"

Die **Funktion "FixhzFreeGroupsCallback"** ist eine anwendungsdefinierte Funktion, die den von der [**Funktion "AghzComputeGroupsCallback"**](authzcomputegroupscallback.md) zugewiesenen Arbeitsspeicher frei gibt. **HzFreeGroupsCallback** ist ein Platzhalter für den anwendungsdefinierten Funktionsnamen.

## <a name="syntax"></a>Syntax


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSidAttrArray* \[ In\]
</dt> <dd>

Ein Zeiger auf den arbeitsspeicherbelegten Speicher, der [**vonHzComputeGroupsCallback zugeordnet wird.**](authzcomputegroupscallback.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Rückruffunktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Attributvariablen müssen in Form eines Ausdrucks sein, wenn sie mit logischen Operatoren verwendet werden. andernfalls werden sie als unbekannt ausgewertet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                   |
| Verteilbare Komponente<br/>          | Windows Server 2003 Administration Tools Pack unter Windows XP<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Grundlegende Access Control Funktionen](authorization-functions.md)
</dt> <dt>

[**HzComputeGroupsCallback**](authzcomputegroupscallback.md)
</dt> </dl>

 

 




