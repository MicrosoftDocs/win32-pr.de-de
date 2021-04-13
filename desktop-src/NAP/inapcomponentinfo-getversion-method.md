---
title: Inapcomponentinfo GetVersion-Methode (napcommon. h)
description: Wird vom NAP-System verwendet, um die Version eines Integritäts Clients zu erhalten.
ms.assetid: aabd13d9-d2ad-4554-a9f6-7845e6775ccd
keywords:
- GetVersion-Methode NAP
- GetVersion-Methode NAP, inapcomponentinfo-Schnittstelle
- Inapcomponentinfo Interface NAP, GetVersion-Methode
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
ms.openlocfilehash: fa1d62c22acf778430bfc2f9dc0e969887c7b306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519180"
---
# <a name="inapcomponentinfogetversion-method"></a>Inapcomponentinfo:: GetVersion-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapcomponentinfo:: GetVersion** -Rückruf Methode wird vom NAP-System verwendet, um die Version eines Integritäts Clients zu erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVersion(
  [out] MessageId *version
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Version* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**MessageId**](nap-datatypes.md) , die die Ressourcen-ID der Version enthält.

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

 

 





