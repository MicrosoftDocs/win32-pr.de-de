---
title: INapComponentInfo GetVendorName-Methode (NapCommon.h)
description: Wird vom NAP-System verwendet, um den Herstellernamen eines Integritätsclients zu erhalten.
ms.assetid: 7083b0b6-38fc-4c24-a5f7-fe0a1ebd5e88
keywords:
- GetVendorName-Methode NAP
- GetVendorName-Methode NAP, INapComponentInfo-Schnittstelle
- INapComponentInfo-Schnittstelle NAP, GetVendorName-Methode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVendorName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d379df4b68ac9aaec42bbe92f02637619b7cf87e0b2cc0d2f1121dec56090baf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799695"
---
# <a name="inapcomponentinfogetvendorname-method"></a>INapComponentInfo::GetVendorName-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapComponentInfo::GetVendorName-Rückrufmethode** wird vom NAP-System verwendet, um den Herstellernamen eines Integritätsclients zu erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVendorName(
  [out] MessageId *vendorName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vendorName* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**MessageId,**](nap-datatypes.md) die die Ressourcen-ID des Herstellernamens enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen dieser Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

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

 

 





