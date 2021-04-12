---
title: WSMAN. enumerationflagreturnobjectandepr-Methode (WSManDisp. h)
description: Gibt den Wert des Enumerationsflags enumerationflagreturnobjectandepr zurück, der im flags-Parameter von Session. Enumerate verwendet werden soll.
ms.assetid: 052b93df-8a83-4b5e-8325-1ad500b43a88
ms.tgt_platform: multiple
keywords:
- Enumerationflagreturnobjectandepr-Methode Windows-Remoteverwaltung
- Enumerationflagreturnobjectandepr-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, enumerationflagreturnobjectandepr-Methode
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObjectAndEPR
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187f8c029d0392ad9ac1a909e1e45de165815e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478657"
---
# <a name="wsmanenumerationflagreturnobjectandepr-method"></a>WSMAN. enumerationflagreturnobjectandepr-Methode

Die **enumerationflagreturnobjectandepr** -Methode gibt den Wert des **Enumerationsflags enumerationflagreturnobjectandepr** für die Verwendung im *Flags* -Parameter von [**Session. Enumerate**](session-enumerate.md)zurück. Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen. Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).

**Enumerationflagreturnobjectandepr** ist eine Konstante in der **\_ wsmanenumflags** -Enumeration und wird in [**Enumerationskonstanten**](enumeration-constants.md)beschrieben.

## <a name="syntax"></a>Syntax


```VB
WSMan.EnumerationFlagReturnObjectAndEPR( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ vorgenommen\]
</dt> <dd>

Der Wert der Konstante.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WSMAN**](wsman.md)
</dt> <dt>

[**Sitzung**](session.md)
</dt> </dl>

 

 





