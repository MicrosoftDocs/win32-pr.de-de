---
title: INapComponentInfo GetLocalizedString-Methode (NapCommon.h)
description: Wird vom NAP-System verwendet, um lokalisierte Zeichenfolgen abzurufen.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- NAP-Methode "GetLocalizedString"
- GetLocalizedString-Methode NAP, INapComponentInfo-Schnittstelle
- INapComponentInfo-Schnittstelle NAP , GetLocalizedString-Methode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetLocalizedString
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be55595bf6c5af6e435d9c53c9b473a721005699da494319ba55eaa828da2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134363"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a>INapComponentInfo::GetLocalizedString-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **Rückrufmethode INapComponentInfo::GetLocalizedString** wird vom NAP-System verwendet, um lokalisierte Zeichenfolgen abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*msgId* \[ In\]
</dt> <dd>

Eine [**MessageId,**](nap-datatypes.md) die die Ressourcen-ID der zu lokalisierenden Zeichenfolge enthält.

</dd> <dt>

*Zeichenfolge* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**CountedString,**](/windows/win32/api/naptypes/ns-naptypes-countedstring) die die lokalisierte Version der Nachricht enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen dieser Fehlercodes zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Zeichenfolgen sollten entsprechend der Sprach-ID des aufrufenden Threads lokalisiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





