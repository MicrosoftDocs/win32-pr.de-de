---
title: Inapsohprocessor GetAttribute-Methode (napprotocol. h)
description: Ruft den Attributtyp und-Wert ab, wenn der Attribut Speicherort angegeben ist.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- GetAttribute-Methode NAP
- GetAttribute-Methode NAP, inapsohprocessor-Schnittstelle
- Inapsohprocessor-Schnittstelle NAP, GetAttribute-Methode
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2d7d9cbafa5a44e0f6c24f4c42959c456722a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340765"
---
# <a name="inapsohprocessorgetattribute-method"></a>Inapsohprocessor:: GetAttribute-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsohprocessor:: GetAttribute** -Methode ruft den Attributtyp und-Wert ab, wenn der Speicherort des Attributs angegeben ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*attributelokation* \[ in\]
</dt> <dd>

Der Speicherort (Index) des Attributs, dessen Typ und Wert abgerufen werden sollen. Der Wert von *attributelokation* wird von einem vorherigen [**inapsohprocessor:: findnextattribute**](inapsohprocessor-findnextattribute-method.md)-Rückruf zurückgegeben.

</dd> <dt>

*Typ* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**sohattributetype**](sohattributetype-enum.md) -Struktur, die den Typ des Attributs im *Wert* angibt.

</dd> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**sohattributevalue**](sohattributevalue-union.md) -Struktur, die den Wert des Attributs gemäß der Definition durch den *Typ* enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
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

[**Inapsohprocessor**](inapsohprocessor.md)
</dt> </dl>

 

 





