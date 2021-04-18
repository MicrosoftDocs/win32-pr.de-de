---
description: Die Put \_ localparticipanttypeer-Methode legt Teilnehmer Informationen fest.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: Itlocalteilnehmer::p ut_LocalParticipantTypedInfo-Methode (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77809a9a3858b6a098fa3ff6a93878cf38518f92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354677"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a>Itlocalteilnehmer::p UT \_ localparticipanttypeer-Methode

Die **Put \_ localparticipanttypeer** -Methode legt Teilnehmer Informationen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*InfoType* \[ in\]
</dt> <dd>

[**Teilnehmer \_ Der typisierte \_ Info**](participant-typed-info.md) Bezeichner des Typs der erforderlichen Informationen.

</dd> <dt>

*ppinfo* \[ in\]
</dt> <dd>

**BSTR** , das den für die Informationen erforderlichen neuen Wert enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss " [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *ppinfo* -Parameter zuzuweisen, und " [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itlocalteilnehmer**](itlocalparticipant.md)
</dt> <dt>

[**\_typisierte Teilnehmer \_ Informationen**](participant-typed-info.md)
</dt> </dl>

 

