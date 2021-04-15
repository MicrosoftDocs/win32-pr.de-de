---
title: Inapcomponentinfo getvendorname-Methode (napcommon. h)
description: Wird vom NAP-System verwendet, um den Herstellernamen eines Integritäts Clients zu erhalten.
ms.assetid: 7083b0b6-38fc-4c24-a5f7-fe0a1ebd5e88
keywords:
- Getvendorname-Methode NAP
- Getvendorname-Methode NAP, inapcomponentinfo-Schnittstelle
- Inapcomponentinfo Interface NAP, getvendorname-Methode
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
ms.openlocfilehash: d3c82f4e7e4f76d827e71421c467a8a223428a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479359"
---
# <a name="inapcomponentinfogetvendorname-method"></a>Inapcomponentinfo:: getvendorname-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapcomponentinfo:: getvendorname** -Rückruf Methode wird vom NAP-System verwendet, um den Herstellernamen eines Integritäts Clients zu erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVendorName(
  [out] MessageId *vendorName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VendorName* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**MessageId**](nap-datatypes.md) , die die Ressourcen-ID des Hersteller namens enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen dieser Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Napcommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcommon. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**Inapcomponentinfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





