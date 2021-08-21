---
title: INapComponentInfo GetIcon-Methode (NapCommon.h)
description: Wird vom NAP-System verwendet, um das Symbol eines Integritätsclients zu erhalten.
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- GetIcon-Methode NAP
- GetIcon-Methode NAP, INapComponentInfo-Schnittstelle
- INapComponentInfo-Schnittstelle NAP, GetIcon-Methode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1711c186d107418d95ccaf19e2a1440b0cecfc0e32fc8c425754d2d9fc19a9d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134434"
---
# <a name="inapcomponentinfogeticon-method"></a>INapComponentInfo::GetIcon-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapComponentInfo::GetIcon-Rückrufmethode** wird vom NAP-System verwendet, um das Symbol eines Integritätsclients zu erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dllFilePath* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf [**countedString,**](/windows/win32/api/naptypes/ns-naptypes-countedstring) der verwendet wird, um den Dateipfad der DLL zurück zu geben, die das Symbol enthält.

</dd> <dt>

*iconResourceId* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Wert, der verwendet wird, um die Ressourcen-ID des zu verwendenden Symbols zurück zu geben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen dieser Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Symbole sollten entsprechend der Sprach-ID des aufrufenden Threads lokalisiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





