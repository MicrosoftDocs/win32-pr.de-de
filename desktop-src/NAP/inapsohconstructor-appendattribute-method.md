---
title: Inapsohconstructor appendattribute-Methode (napprotocol. h)
description: Fügt ein TLV am Ende des SoH-Puffers hinzu.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- Appendattribute-Methode NAP
- Appendattribute-Methode NAP, inapsohconstructor-Schnittstelle
- Inapsohconstructor Interface NAP, appendattribute-Methode
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
ms.openlocfilehash: cc10fad9c775d324822700b77afed4e65a798db6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517708"
---
# <a name="inapsohconstructorappendattribute-method"></a>Inapsohconstructor:: appendattribute-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsohconstructor:: appendattribute** -Methode fügt ein TLV am Ende des SoH-Puffers hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* \[ in\]
</dt> <dd>

Eine [**sohattributetype**](sohattributetype-enum.md) -Enumeration, die den Attributtyp des neuen TLV angibt.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**sohattributevalue**](sohattributevalue-union.md) -Struktur, die den Wert für das neue TLV enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der TLV " [**sohattributetypesystemhealthid**](sohattributetype-enum.md) " darf nicht mit dieser Funktion hinzugefügt werden. Es wird als erstes TLV von [**inapsohconstructor:: Initialize**](inapsohconstructor-initialize-method.md) zu neu erstellten SoH-Paketen hinzugefügt.

Wenn ein Attribut angehängt wird, das vom NAP-System genutzt wird, sollte es nicht verschlüsselt oder geändert werden. Wenn die Integritäts Entität eine Verschlüsselung/Integritäts Überprüfung (Macs) privater Informationen erfordert, sollte Sie nur in das [**sohattributetypevendorspecific**](sohattributetype-enum.md) -Attribut eingeschlossen werden.

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

 

 





