---
title: INapSoHProcessor FindNextAttribute-Methode (NapProtocol.h)
description: Sucht den Speicherort (Index) des nächsten Attributs des durch SoHAttributeType angegebenen Typs.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- FindNextAttribute-Methode NAP
- FindNextAttribute-Methode NAP, INapSoHProcessor-Schnittstelle
- INapSoHProcessor-Schnittstelle NAP, FindNextAttribute-Methode
topic_type:
- apiref
api_name:
- INapSoHProcessor.FindNextAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4425707487994904d1bd2a622cd1ab66f286469c93e80a8eb01e71c0319426ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939577"
---
# <a name="inapsohprocessorfindnextattribute-method"></a>INapSoHProcessor::FindNextAttribute-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapSoHProcessor::FindNextAttribute-Methode** sucht den Speicherort (Index) des nächsten Attributs des Typs, der durch *SoHAttributeType angegeben wird.*

## <a name="syntax"></a>Syntax


```C++
HRESULT FindNextAttribute(
  [in]  UINT16           fromLocation,
  [in]  SoHAttributeType type,
  [out] UINT16           *attributeLocation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fromLocation* \[ In\]
</dt> <dd>

Der Startort (Index) im SoH-Paket (Statement of Health), um die Attributsuche zu starten. Dieser Wert muss im Bereich von 0 bis (**numAttrib** - 1) liegen, wobei **numAttrib** mithilfe von [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md)abgerufen wird.

> [!Note]  
> Das SoH-Paket verwendet 0-basierte Attributindizes.

 

</dd> <dt>

*type* \[ In\]
</dt> <dd>

Eine [**SoHAttributeType-Struktur,**](sohattributetype-enum.md) die den zu suchenden Attributtyp enthält.

</dd> <dt>

*attributeLocation* \[ out\]
</dt> <dd>

Ein Zeiger, der den Speicherort (Index) im SoH-Paket des ersten Attributs vom *Typ SoHAttributeType* aus dem Index *fromLocation enthält.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                            | Beschreibung                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |
| <dl> <dt>**FEHLERDATEI \_ \_ NICHT \_ GEFUNDEN**</dt> </dl> | Das Attribut wurde nicht gefunden.<br/>                                    |



 

## <a name="remarks"></a>Hinweise

Die **FindNextAttribute-Methode** sucht nach Attributen des *Typs SoHAttributeType* aus dem von *fromLocation* angegebenen Index und höher, bis eine Übereinstimmung gefunden wird. Wenn keine Übereinstimmung gefunden wird, **wird ERROR FILE NOT \_ \_ \_ FOUND** zurückgegeben.

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

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





