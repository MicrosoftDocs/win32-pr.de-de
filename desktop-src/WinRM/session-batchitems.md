---
title: Session.BatchItems-Eigenschaft (WSManDisp.h)
description: Legt die Anzahl der Elemente in jedem Enumerationsbatch fest und ruft sie ab.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- BatchItems-Eigenschaft Windows Remoteverwaltung
- BatchItems-Eigenschaft Windows Remoteverwaltung, Sitzungsobjekt
- Sitzungsobjekt Windows Remoteverwaltung, BatchItems-Eigenschaft
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
ms.openlocfilehash: 59e395eb27be2b922cf9d53e40f1d8cea0fc13a5dcf7b62b95ac606ec8f3f96f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795340"
---
# <a name="sessionbatchitems-property"></a>Session.BatchItems-Eigenschaft

Legt die Anzahl der Elemente in jedem Enumerationsbatch fest und ruft sie ab. Dieser Wert kann während einer Enumeration nicht geändert werden. Der Ressourcenanbieter kann einen Grenzwert festlegen.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Session.BatchItems As long
```



## <a name="property-value"></a>Eigenschaftswert

Gibt die maximale Anzahl von Elementen an, die für jeden zugrunde liegenden Netzwerkaufruf an den Dienst zurückgegeben werden. Der Standardwert ist 20.

## <a name="remarks"></a>Hinweise

Dies ist ein Optimierungsfeature, das steuert, wie oft Netzwerkaufrufe zwischen dem Client und dem Server ausgeführt werden. Derzeit wird es nur für Enumerationen verwendet. Weitere Informationen zum Aufzählen von Ressourcen finden Sie unter [**Aufzählen von**](session-enumerate.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Sitzungskonsistenz**](session.md)
</dt> <dt>

[**Aufzählen**](session-enumerate.md)
</dt> <dt>

[**Enumerator.ReadItem**](enumerator-readitem.md)
</dt> </dl>

 

 





