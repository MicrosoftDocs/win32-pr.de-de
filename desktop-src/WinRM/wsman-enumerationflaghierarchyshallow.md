---
title: WSMAN. enumerationflaghierarchyflache-Methode (WSManDisp. h)
description: Gibt den Wert des Enumerationsflags enumerationflaghierarchyflache zurück, der im flags-Parameter von Session. Enumerate verwendet werden soll.
ms.assetid: 18b564e6-dda1-44b9-b445-26c6183b6af9
ms.tgt_platform: multiple
keywords:
- Enumerationflaghierarchyflache-Methode Windows-Remoteverwaltung
- Enumerationflaghierarchyflache-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, enumerationflaghierarchyflache-Methode
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyShallow
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b74552fd88ac370ad4a3f8b885a7f61e65a053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518140"
---
# <a name="wsmanenumerationflaghierarchyshallow-method"></a>WSMAN. enumerationflaghierarchyflache-Methode

Die **enumerationflaghierarchyflache** -Methode gibt den Wert des **Enumerationsflags enumerationflaghierarchyflache** zurück, der im *Flags* -Parameter von [**Session. Enumerate**](session-enumerate.md)verwendet werden soll. Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen. Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).

**Enumerationflaghierarchyflache** ist eine Konstante in der **\_ wsmanenumflags** -Enumeration und wird in [**Enumerationskonstanten**](enumeration-constants.md)beschrieben.

## <a name="syntax"></a>Syntax


```VB
WSMan.EnumerationFlagHierarchyShallow( _
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

 

 





