---
description: Die get \_ localparticipanttypeer-Methode ruft Teilnehmer Informationen ab, wie z. b. den e-Mail-Namen oder den geografischen Standort.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'Itlocalteilnehmer:: get_LocalParticipantTypedInfo-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabaf503963c09898c06659884fd3ac3858e704
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355979"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a>Itlocalteilnehmer:: get \_ localparticipanttypdinfo-Methode

Die **get \_ localparticipanttypeer** -Methode ruft Teilnehmer Informationen ab, wie z. b. den e-Mail-Namen oder den geografischen Standort.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*InfoType* \[ in\]
</dt> <dd>

[**Teilnehmer \_ Der typisierte \_ Info**](participant-typed-info.md) Bezeichner vom Typ der erforderlichen Informationen.

</dd> <dt>

*ppinfo* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen **BSTR** -Wert, der die erforderlichen Informationen nach der erfolgreichen Rückgabe der Methode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppinfo* -Parameter zugewiesenen Arbeitsspeicher freizugeben.

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

 

