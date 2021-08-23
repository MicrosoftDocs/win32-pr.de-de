---
title: INapSoHConstructor AppendAttribute-Methode (NapProtocol.h)
description: Fügt am Ende des SoH-Puffers einen TLV hinzu.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- AppendAttribute-Methode NAP
- AppendAttribute-Methode NAP, INapSoHConstructor-Schnittstelle
- INapSoHConstructor-Schnittstelle NAP, AppendAttribute-Methode
topic_type:
- apiref
api_name:
- INapSoHConstructor.AppendAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7d7ca4636d0eaeea35054dc5330b17f1360dffec5231922ad0acc357231c3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939587"
---
# <a name="inapsohconstructorappendattribute-method"></a>INapSoHConstructor::AppendAttribute-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapSoHConstructor::AppendAttribute-Methode** fügt am Ende des SoH-Puffers einen TLV hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*type* \[ In\]
</dt> <dd>

Eine [**SoHAttributeType-Enumeration,**](sohattributetype-enum.md) die den Attributtyp des neuen TLV angibt.

</dd> <dt>

*value* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**SoHAttributeValue-Struktur,**](sohattributevalue-union.md) die den Wert für den neuen TLV enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Das [**TLV sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) darf nicht mit dieser Funktion hinzugefügt werden. Es wird als erstes TLV von [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md) zu neu erstellten SOH-Paketen hinzugefügt.

Beim Anfügen eines Attributs, das vom Nap-System verwendet wird, sollte es nicht verschlüsselt oder in irgendeiner Weise geändert werden. Wenn HealthEntity eine Verschlüsselungs-/Integritätsüberprüfung (ENCRYPTION/Integrity Checking, MACs) privater Informationen erfordert, sollte sie nur im [**attribut sohAttributeTypeVendorSpecific enthalten**](sohattributetype-enum.md) sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





