---
title: Inapcomponentinfo-GetIcon-Methode (napcommon. h)
description: Wird vom NAP-System verwendet, um das Symbol eines Integritäts Clients zu erhalten.
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- GetIcon-Methode NAP
- GetIcon-Methode NAP, inapcomponentinfo-Schnittstelle
- Inapcomponentinfo-Schnittstelle NAP, GetIcon-Methode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 795ad85f8497262f88fa55d8efb2da7466b8c3a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957083"
---
# <a name="inapcomponentinfogeticon-method"></a>Inapcomponentinfo:: GetIcon-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapcomponentinfo:: GetIcon** -Rückruf Methode wird vom NAP-System verwendet, um das Symbol eines Integritäts Clients zu erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dllfilepath* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**zählzeichenfolge**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , die verwendet wird, um den Dateipfad der dll zurückzugeben, die das Symbol enthält.

</dd> <dt>

*IconResourceID* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Wert, der verwendet wird, um die Ressourcen-ID des zu verwendenden Symbols zurückzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen dieser Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Symbole sollten entsprechend der Sprach-ID des aufrufenden Threads lokalisiert werden.

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

 

 





