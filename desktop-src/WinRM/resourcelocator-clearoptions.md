---
title: ResourceLocator.ClearOptions-Methode (WSManDisp.h)
description: Entfernt alle Optionen aus dem ResourceLocator-Objekt.
ms.assetid: 1b4d7f15-c56f-4b0d-9614-8376012abca7
ms.tgt_platform: multiple
keywords:
- ClearOptions-Methode Windows Remoteverwaltung
- ClearOptions-Methode Windows Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows Remoteverwaltung , ClearOptions-Methode
topic_type:
- apiref
api_name:
- ResourceLocator.ClearOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef695b949c62c0d56de45914e1a54996d4d7599f029d136ad78b03ac687365aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112911"
---
# <a name="resourcelocatorclearoptions-method"></a>ResourceLocator.ClearOptions-Methode

Entfernt alle Optionen [*aus*](windows-remote-management-glossary.md) dem [**ResourceLocator-Objekt.**](resourcelocator.md) Sie können ein [**ResourceLocator-Objekt**](resourcelocator.md) bereitstellen, anstatt [**in**](session.md) Sitzungsobjektvorgängen wie [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)oder [**Session.Enumerate einen Ressourcen-URI anzugeben.**](session-enumerate.md)

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.ClearOptions()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="remarks"></a>Hinweise

**IWSManResourceLocator::ClearOptions** ist die entsprechende C++-Methode.

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

 

 





