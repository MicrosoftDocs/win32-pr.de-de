---
description: Die put \_ LocalParticipantTypedInfo-Methode legt Teilnehmerinformationen fest.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: ITLocalParticipant::p ut_LocalParticipantTypedInfo-Methode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acca83d7ad68ed0974aaa2e7d4fb4755c11939d0711473c406cb09d78451ac41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774900"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a>ITLocalParticipant::p ut \_ LocalParticipantTypedInfo-Methode

Die **put \_ LocalParticipantTypedInfo-Methode** legt Teilnehmerinformationen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*InfoType* \[ In\]
</dt> <dd>

[**TEILNEHMER \_ TYPED \_ INFO-Bezeichner**](participant-typed-info.md) des erforderlichen Informationstyps.

</dd> <dt>

*ppInfo* \[ In\]
</dt> <dd>

**BSTR** mit dem erforderlichen neuen Wert für die Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die Anwendung muss [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) verwenden, um Arbeitsspeicher für den *ppInfo-Parameter* zu reservieren, und [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher frei zu geben, wenn die Variable nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITLocalParticipant**](itlocalparticipant.md)
</dt> <dt>

[**VOM \_ TEILNEHMER TYPIERTE \_ INFORMATIONEN**](participant-typed-info.md)
</dt> </dl>

 

