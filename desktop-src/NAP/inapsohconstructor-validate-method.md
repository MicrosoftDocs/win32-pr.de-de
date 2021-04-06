---
title: Inapsohconstructor Validate-Methode (napprotocol. h)
description: Überprüft die Gültigkeit des SoH-Pakets.
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- Validate-Methode für NAP
- Validate-Methode, NAP, inapsohconstructor-Schnittstelle
- Inapsohconstructor-Schnittstelle NAP, Validate-Methode
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742608"
---
# <a name="inapsohconstructorvalidate-method"></a>Inapsohconstructor:: Validate-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsohconstructor:: Validate** -Methode überprüft die Gültigkeit des SoH-Pakets.

## <a name="syntax"></a>Syntax


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SoH* \[ in\]
</dt> <dd>

Ein Zeiger auf das erstellte [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket.

</dd> <dt>

*isrequest* \[ in\]
</dt> <dd>

Ein **boolescher** Wert, der **true** ist, wenn das Paket ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) und **false** ist, wenn es sich um eine **sohresponse** handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                            | Beschreibung                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Das SoH-Paket ist gültig.<br/>                                |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl>        | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>         | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |
| <dl> <dt>**\_ \_ Ungültiges NAP- \_ Paket**</dt> </dl> | Das SoH-Paket ist ungültig.<br/>                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Napprotocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napprotocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsohconstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





