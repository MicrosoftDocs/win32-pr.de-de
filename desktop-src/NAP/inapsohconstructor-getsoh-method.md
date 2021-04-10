---
title: Inapsohconstructor getsoh-Methode (napprotocol. h)
description: Ruft das erstellte sohrequest-oder sohresponse-Paket ab.
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- Getsoh-Methode NAP
- Getsoh-Methode NAP, inapsohconstructor-Schnittstelle
- Inapsohconstructor Interface NAP, getsoh-Methode
topic_type:
- apiref
api_name:
- INapSoHConstructor.GetSoH
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066257aadf0ed14816efec06936d4b070087159f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103538"
---
# <a name="inapsohconstructorgetsoh-method"></a>Inapsohconstructor:: getsoh-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsohconstructor:: getsoh** -Methode ruft das erstellte sohrequest-oder sohresponse-Paket ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SoH* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf das erstellte [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -oder **sohresponse** -Paket.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

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

 

 





