---
title: INapComponentInfo GetFriendlyName-Methode (NapCommon.h)
description: Wird vom NAP-System verwendet, um den Anzeigenamen eines Integritätsclients abzurufen.
ms.assetid: 28614f06-a250-4f92-abf2-422675efd8a0
keywords:
- GetFriendlyName-Methode NAP
- GetFriendlyName-Methode NAP, INapComponentInfo-Schnittstelle
- INapComponentInfo-Schnittstelle NAP , GetFriendlyName-Methode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetFriendlyName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3236a9d4959c441816aa476993d95286b4ac1f710ccdb63325aba225bfabb106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799715"
---
# <a name="inapcomponentinfogetfriendlyname-method"></a>INapComponentInfo::GetFriendlyName-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **Rückrufmethode INapComponentInfo::GetFriendlyName** wird vom NAP-System verwendet, um den Anzeigenamen eines Integritätsclients abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFriendlyName(
  [out] MessageId *friendlyName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*friendlyName* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**MessageId,**](nap-datatypes.md) die die Ressourcen-ID des Anzeigenamens enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen dieser Fehlercodes zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





