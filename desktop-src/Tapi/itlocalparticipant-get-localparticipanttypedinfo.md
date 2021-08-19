---
description: Die get \_ LocalParticipantTypedInfo-Methode ruft Teilnehmerinformationen ab, z. B. E-Mail-Name oder geografischer Standort.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: ITLocalParticipant::get_LocalParticipantTypedInfo-Methode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41afb4c55ba769e341b81e5ec1ca721745509ba8bf2bdfd88ae22ebc48bb535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003368"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a>ITLocalParticipant::get \_ LocalParticipantTypedInfo-Methode

Die **get \_ LocalParticipantTypedInfo-Methode** ruft Teilnehmerinformationen ab, z. B. E-Mail-Name oder geografischer Standort.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*InfoType* \[ In\]
</dt> <dd>

[**TEILNEHMER \_ TYPED \_ INFO-Bezeichner**](participant-typed-info.md) des erforderlichen Informationstyps.

</dd> <dt>

*ppInfo* \[ out\]
</dt> <dd>

Zeiger auf einen **BSTR,** der die erforderlichen Informationen nach einer erfolgreichen Rückgabe der Methode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die Anwendung muss [SysFreeString verwenden,](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) um den für den *ppInfo-Parameter* zugeordneten Arbeitsspeicher frei zu geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITLocalParticipant**](itlocalparticipant.md)
</dt> <dt>

[**VOM \_ TEILNEHMER TYPIERTE \_ INFORMATIONEN**](participant-typed-info.md)
</dt> </dl>

 

