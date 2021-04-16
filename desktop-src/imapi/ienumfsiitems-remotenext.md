---
title: Ienumf siitems RemoteNext-Methode
description: Unterstützt einen Remote Client, der eine angegebene Anzahl von Elementen in der enumerationssequenz abrufen möchte. | Ienumf siitems RemoteNext-Methode
ms.assetid: a5ae59ed-08d7-4225-9aec-91049789e8fe
keywords:
- RemoteNext-Methode IMAPI
- RemoteNext-Methode IMAPI, ienumssiitems-Schnittstelle
- Ienumf siitems Interface IMAPI, RemoteNext-Methode
topic_type:
- apiref
api_name:
- IEnumFsiItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e29d3f75cd8e2f83fcd21236661d0d1fa0dabef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530713"
---
# <a name="ienumfsiitemsremotenext-method"></a>Ienumf siitems:: RemoteNext-Methode

Unterstützt einen Remote Client, der eine angegebene Anzahl von Elementen in der enumerationssequenz abrufen möchte.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoteNext(
  [in]  ULONG    celt,
  [out] IFsiItem **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*celt* \[ in\]
</dt> <dd>

Anzahl der abzurufenden Elemente.

</dd> <dt>

*rgelt* \[ vorgenommen\]
</dt> <dd>

Array von [**ifsiitem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) -Schnittstellen. Wenn Sie den Vorgang abgeschlossen haben, müssen Sie jede Schnittstelle in rgelt freigeben

</dd> <dt>

*pceltfetch* \[ vorgenommen\]
</dt> <dd>

Anzahl der Elemente, die in rgelt zurückgegeben werden. Sie können *pceltfetch* auf **null** festlegen, wenn es sich um ein *celt* handelt. Initialisieren Sie andernfalls den Wert von *pceltfetch* auf 0, bevor Sie diese Methode aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

S \_ OK wird zurückgegeben, wenn die Anzahl der angeforderten Elemente (*celt*) erfolgreich zurückgegeben wurde oder wenn die Anzahl der zurückgegebenen Elemente (*pceltfetch*) kleiner als die Anzahl der angeforderten Elemente ist.

Andere Erfolgs Codes können als Ergebnis der-Implementierung zurückgegeben werden. Die folgenden Fehlercodes werden häufig bei einem Vorgangs Fehler zurückgegeben. Sie stellen jedoch nicht die einzigen möglichen Fehler Werte dar:



| Rückgabecode                                                                                   | Beschreibung                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Der Zeiger ist ungültig.<br/> Wert: 0x80004003<br/>                   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Der erforderliche Arbeitsspeicher konnte nicht belegt werden.<br/> Wert: 0x8007000E<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Mindestens ein Argument ist ungültig.<br/> Wert: 0x80070057<br/>    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP2 \[ Desktop-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| IDL<br/>                      | <dl> <dt>Imapi2fs. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ienumssiitems**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems)
</dt> <dt>

[Ienumssiitems:: Next](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumfsiitems-next)
</dt> </dl>

 

 





