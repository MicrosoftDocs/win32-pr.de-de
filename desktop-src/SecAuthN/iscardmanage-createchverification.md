---
description: Erstellt eine ISCardVerify-Schnittstelle.
ms.assetid: 6338e672-83cd-46fe-8f94-f4ba6e2581ea
title: ISCardManage::CreateCHVerification-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCHVerification
api_type:
- COM
api_location: ''
ms.openlocfilehash: 312fc18be42ccc7ba35a0d0a6288637bd92cd0f10a855dc95c457329c69cd7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922767"
---
# <a name="iscardmanagecreatechverification-method"></a>ISCardManage::CreateCHVerification-Methode

\[Die **CreateCHVerification-Methode** ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **CreateCHVerification-Methode** erstellt eine [**ISCardVerify-Schnittstelle.**](iscardverify.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateCHVerification(
  [out] ISCardVerify **ppISCardVerify
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppISCardVerify* \[ out\]
</dt> <dd>

Zeiger auf die erstellte [**ISCardVerify-Schnittstelle**](iscardverify.md) zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Der *ppISCardVerify-Parameter* ist ungültig.<br/>  |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Ein fehlerhafter Zeiger wurde in *ppISCardVerify übergeben.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                |



 

## <a name="remarks"></a>Hinweise

Eine Liste aller von dieser Schnittstelle definierten Methoden finden Sie unter [**ISCardManage**](iscardmanage.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes [](../secgloss/s-gly.md) gibt diese Schnittstelle möglicherweise einen Smartcardfehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**ISCardVerify**](iscardverify.md)
</dt> </dl>

 

 
