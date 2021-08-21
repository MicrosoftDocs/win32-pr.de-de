---
title: INapSoHConstructor GetSoH-Methode (NapProtocol.h)
description: Ruft das konstruierte SoHRequest- oder SoHResponse-Paket ab.
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- GetSoH-Methode NAP
- GetSoH-Methode NAP, INapSoHConstructor-Schnittstelle
- INapSoHConstructor-Schnittstelle NAP, GetSoH-Methode
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
ms.openlocfilehash: d3d411d57ae77a1e5bf8c04ca0d9d980a9c33e9fcf15eb05f157ddeda98711c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133823"
---
# <a name="inapsohconstructorgetsoh-method"></a>INapSoHConstructor::GetSoH-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapSoHConstructor::GetSoH-Methode** ruft das konstruierte SoHRequest- oder SoHResponse-Paket ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*soh* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf das konstruierte [**SoHRequest-**](/windows/win32/api/naptypes/ns-naptypes-soh) oder **SoHResponse-Paket.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





