---
title: INapComponentInfo GetVersion-Methode (NapCommon.h)
description: Wird vom NAP-System verwendet, um die Version eines Integritätsclients abzurufen.
ms.assetid: aabd13d9-d2ad-4554-a9f6-7845e6775ccd
keywords:
- GetVersion-Methode NAP
- GetVersion-Methode NAP, INapComponentInfo-Schnittstelle
- INapComponentInfo-Schnittstelle NAP , GetVersion-Methode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVersion
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e815c7d92ba9a33c07ba4d8d68c588ed0014019d0d173e0304c4a10204d4d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368382"
---
# <a name="inapcomponentinfogetversion-method"></a>INapComponentInfo::GetVersion-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **Rückrufmethode INapComponentInfo::GetVersion** wird vom NAP-System verwendet, um die Version eines Integritätsclients abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVersion(
  [out] MessageId *version
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Version* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**MessageId,**](nap-datatypes.md) die die Ressourcen-ID der Version enthält.

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

 

 





