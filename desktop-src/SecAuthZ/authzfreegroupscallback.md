---
description: Eine Anwendungs definierte Funktion, die von der authzcomputegroupscallback-Funktion zugeordnete Arbeitsspeicher freigibt. Authzfregroupscallback ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: Authzfregroupscallback-Rückruffunktion
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
ms.openlocfilehash: 7d8942acbc67f122ea79f0b9e98793628b5f21f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760825"
---
# <a name="authzfreegroupscallback-callback-function"></a>Authzfregroupscallback-Rückruffunktion

Die **authzfregroupscallback** -Funktion ist eine Anwendungs definierte Funktion, die von der [**authzcomputegroupscallback**](authzcomputegroupscallback.md) -Funktion zugeordnete Arbeitsspeicher freigibt. **Authzfregroupscallback** ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.

## <a name="syntax"></a>Syntax


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psidattrarray* \[ in\]
</dt> <dd>

Ein Zeiger auf den von [**authzcomputegroupscallback**](authzcomputegroupscallback.md)zugeordneten Arbeitsspeicher.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Rückruffunktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Attribut Variablen müssen in Form eines Ausdrucks vorliegen, wenn Sie mit logischen Operatoren verwendet werden. Andernfalls werden Sie als UNKNOWN ausgewertet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                   |
| Verteilbare Komponente<br/>          | Windows Server 2003-Verwaltungs Tools Pack unter Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Grundlegende Access Control Funktionen](authorization-functions.md)
</dt> <dt>

[**Authzcomputegroupscallback**](authzcomputegroupscallback.md)
</dt> </dl>

 

 




