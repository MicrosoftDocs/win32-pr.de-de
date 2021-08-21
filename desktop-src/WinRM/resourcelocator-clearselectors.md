---
title: ResourceLocator.ClearSelectors-Methode (WSManDisp.h)
description: Entfernt alle Selektoren aus einem ResourceLocator-Objekt.
ms.assetid: 759880e6-5026-45de-b7e1-a4f5a16c32a0
ms.tgt_platform: multiple
keywords:
- ClearSelectors-Methode Windows Remoteverwaltung
- ClearSelectors-Methode Windows Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows Remoteverwaltung, ClearSelectors-Methode
topic_type:
- apiref
api_name:
- ResourceLocator.ClearSelectors
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d54fda16aa67086304e62b4c762769cc7dea832437a939f3928eda665623f5ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112836"
---
# <a name="resourcelocatorclearselectors-method"></a>ResourceLocator.ClearSelectors-Methode

Entfernt alle [*Selektoren*](windows-remote-management-glossary.md) aus einem [**ResourceLocator-Objekt.**](resourcelocator.md) Sie können ein [**ResourceLocator-Objekt**](resourcelocator.md) angeben, anstatt einen Ressourcen-URI in [**Sitzungsobjektvorgängen**](session.md) wie [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)oder [**Session.Enumerate**](session-enumerate.md)anzugeben.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.ClearSelectors()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="remarks"></a>Hinweise

**IWSManResourceLocator::ClearSelectors** ist die entsprechende C++-Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Resourcelocator**](resourcelocator.md)
</dt> </dl>

 

 





