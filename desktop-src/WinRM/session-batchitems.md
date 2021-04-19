---
title: Session.Batchitems-Eigenschaft (WSManDisp. h)
description: Legt die Anzahl der Elemente in jedem enumerationsbatch fest und ruft Sie ab.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- Batchitems-Eigenschaft Windows-Remoteverwaltung
- Batchitems-Eigenschaft Windows-Remoteverwaltung, Session-Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, batchitems (Eigenschaft)
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb668b80a2fea8ec5c8683a7a85a20cfbb217a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342651"
---
# <a name="sessionbatchitems-property"></a>Session.Batchitems (Eigenschaft)

Legt die Anzahl der Elemente in jedem enumerationsbatch fest und ruft Sie ab. Dieser Wert kann während einer Enumeration nicht geändert werden. Der Ressourcenanbieter kann ein Limit festlegen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Session.BatchItems As long
```



## <a name="property-value"></a>Eigenschaftswert

Gibt die maximale Anzahl von Elementen an, die für die einzelnen zugrunde liegenden Netzwerk Aufrufe an den Dienst zurückgegeben werden. Der Standardwert ist 20.

## <a name="remarks"></a>Bemerkungen

Dies ist ein Optimierungs Feature, das steuert, wie oft Netzwerk Aufrufe zwischen dem Client und dem Server durchgeführt werden. Derzeit wird Sie nur für Enumerationen verwendet. Weitere Informationen zum Auflisten von Ressourcen finden Sie unter [**Enumerate**](session-enumerate.md).

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

[**Sitzung**](session.md)
</dt> <dt>

[**Aufzählen**](session-enumerate.md)
</dt> <dt>

[**Enumerator. ReadItem**](enumerator-readitem.md)
</dt> </dl>

 

 





