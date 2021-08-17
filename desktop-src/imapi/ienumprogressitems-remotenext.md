---
title: IEnumProgressItems RemoteNext-Methode
description: Unterstützt einen Remoteclient, der eine angegebene Anzahl von Elementen in der Enumerationssequenz abrufen möchte. | IEnumProgressItems RemoteNext-Methode
ms.assetid: c5f85ca3-1bad-49fd-9e67-d41135cd837d
keywords:
- 'RemoteNext-Methode : IMAPI'
- RemoteNext-Methode IMAPI, IEnumProgressItems-Schnittstelle
- IEnumProgressItems-Schnittstelle IMAPI , RemoteNext-Methode
topic_type:
- apiref
api_name:
- IEnumProgressItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daa2b33fdc356782837aadfe37186bc4cc2b493208fdc78ba645ada9e746582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884850"
---
# <a name="ienumprogressitemsremotenext-method"></a>IEnumProgressItems::RemoteNext-Methode

Unterstützt einen Remoteclient, der eine angegebene Anzahl von Elementen in der Enumerationssequenz abrufen möchte.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoteNext(
  [in]  ULONG         celt,
  [out] IProgressItem **rgelt,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Celt* \[ In\]
</dt> <dd>

Anzahl der abzurufende Elemente.

</dd> <dt>

*rgelt* \[ out\]
</dt> <dd>

Array von [**IProgressItem-Schnittstellen.**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) Wenn Sie fertig sind, müssen Sie jede Schnittstelle in rgelt freigeben.

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Anzahl der in rgelt zurückgegebenen Elemente. Sie können *pceltFetched* auf **NULL** festlegen, wenn *celt* eins ist. Andernfalls initialisieren Sie den Wert von *pceltFetched* auf 0, bevor Sie diese Methode aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

S \_ OK wird zurückgegeben, wenn die Anzahl der angeforderten Elemente (*celt*) erfolgreich zurückgegeben wird oder die Anzahl der zurückgegebenen Elemente (*pceltFetched*) kleiner als die Anzahl der angeforderten Elemente ist.

Andere Erfolgscodes können als Ergebnis der Implementierung zurückgegeben werden. Die folgenden Fehlercodes werden häufig bei einem Vorgangsfehler zurückgegeben, stellen jedoch nicht die einzigen möglichen Fehlerwerte dar:



| Rückgabecode                                                                                   | Beschreibung                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Zeiger ist ungültig.<br/> Wert: 0x80004003<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Fehler beim Zuordnen des erforderlichen Arbeitsspeichers.<br/> Wert: 0x8007000E<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Mindestens ein Argument ist ungültig.<br/> Wert: 0x80070057<br/>    |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Unerwarteter Fehler.<br/> Wert: 0x8000FFFF<br/>         |



 

## <a name="remarks"></a>Hinweise

Wenn weniger Elemente als die angeforderte Anzahl von Elementen in der Sequenz vorhanden sind, werden die verbleibenden Elemente abgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP2-Desktop-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Idl<br/>                      | <dl> <dt>Imapi2fs.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumProgressItems**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems)
</dt> <dt>

[IEnumProgressItems::Next](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next)
</dt> </dl>

 

 





