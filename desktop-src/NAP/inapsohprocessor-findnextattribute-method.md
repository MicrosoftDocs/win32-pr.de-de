---
title: Inapsohprocessor findnextattribute-Methode (napprotocol. h)
description: Sucht den Speicherort (Index) des nächsten Attributs des Typs, der von sohattributetype angegeben wird.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- Findnextattribute-Methode NAP
- Findnextattribute-Methode NAP, inapsohprocessor-Schnittstelle
- Inapsohprocessor-Schnittstelle NAP, findnextattribute-Methode
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
ms.openlocfilehash: e1a270e36f8254ed5dbfcd9776cf013f9d10d4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740224"
---
# <a name="inapsohprocessorfindnextattribute-method"></a>Inapsohprocessor:: findnextattribute-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsohprocessor:: findnextattribute** -Methode sucht den Speicherort (Index) des nächsten Attributs des Typs, der von *sohattributetype* angegeben wird.

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

*fromlocation* \[ in\]
</dt> <dd>

Der Start Speicherort (Index) im SoH-Paket (Statement of Health) zum Starten der Attribut Suche. Dieser Wert muss zwischen 0 und (**numatdreib** -1) liegen, wobei **numatdreib** mit [**inapsohprocessor:: getnumofattributes**](inapsohprocessor-getnumberofattributes-method.md)abgerufen wird.

> [!Note]  
> Das SoH-Paket verwendet 0-basierte Attribut Indizes.

 

</dd> <dt>

*Typ* \[ in\]
</dt> <dd>

Eine [**sohattributetype**](sohattributetype-enum.md) -Struktur, die den zu suchenden Attributtyp enthält.

</dd> <dt>

*attributelokation* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger, der den Speicherort (Index) im SoH-Paket des ersten Attributs vom Typ *sohattributetype* aus dem Index *fromlocation* enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                            | Beschreibung                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl>        | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>         | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |
| <dl> <dt>**Fehler \_ Datei \_ nicht \_ gefunden.**</dt> </dl> | Das Attribut wurde nicht gefunden.<br/>                                    |



 

## <a name="remarks"></a>Bemerkungen

Die **findnextattribute** -Methode sucht nach Attributen vom Typ *sohattributetype* aus dem von *fromlocation* angegebenen Index und höher, bis eine Entsprechung gefunden wird. Wenn keine Entsprechung gefunden wird, wird die **Fehler \_ Datei \_ nicht \_ gefunden** .

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

 

 





