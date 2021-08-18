---
title: INapSoHProcessor GetAttribute-Methode (NapProtocol.h)
description: Ruft den Attributtyp und -wert ab, wenn die Attributposition angegeben ist.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- GetAttribute-Methode NAP
- GetAttribute-Methode NAP, INapSoHProcessor-Schnittstelle
- INapSoHProcessor-Schnittstelle NAP, GetAttribute-Methode
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
ms.openlocfilehash: 1ba1b86ca1eab51fdca382a758a9a65650af2249eb0d605c24274c84d1f95669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939567"
---
# <a name="inapsohprocessorgetattribute-method"></a>INapSoHProcessor::GetAttribute-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSoHProcessor::GetAttribute-Methode** ruft den Attributtyp und -wert ab, wenn der Attributspeicherort angegeben ist.

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

*attributeLocation* \[ In\]
</dt> <dd>

Der Speicherort (Index) des Attributs, dessen Typ und Wert abgerufen werden sollen. Der Wert von *attributeLocation* wird von einem vorherigen Aufruf von [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md)zurückgegeben.

</dd> <dt>

*Type (Typ)* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**SoHAttributeType-Struktur,**](sohattributetype-enum.md) die den Typ des Attributs im *Wert* angibt.

</dd> <dt>

*wert* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**SoHAttributeValue-Struktur,**](sohattributevalue-union.md) die den Durch *den Typ* definierten Wert des Attributs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





