---
title: ResourceLocator.AddSelector-Methode (WSManDisp.h)
description: Fügt dem ResourceLocator-Objekt einen Selektor hinzu. Der Selektor gibt eine bestimmte Instanz einer Ressource an.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- AddSelector-Methode Windows Remoteverwaltung
- AddSelector-Methode Windows Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows Remoteverwaltung, AddSelector-Methode
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fc59aab6e5194716fa3b0cda98bb874d0045011c0159c5caaa3cbd53e7fbfd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121640"
---
# <a name="resourcelocatoraddselector-method"></a>ResourceLocator.AddSelector-Methode

Fügt dem [**ResourceLocator-Objekt einen Selektor**](resourcelocator.md) hinzu. [](windows-remote-management-glossary.md) Der Selektor gibt eine bestimmte Instanz einer Ressource *an.* Sie können ein [**ResourceLocator-Objekt**](resourcelocator.md) bereitstellen, anstatt [**in**](session.md) Sitzungsobjektvorgängen wie [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)oder [**Session.Enumerate einen Ressourcen-URI anzugeben.**](session-enumerate.md)

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*resourceSelName* \[ In\]
</dt> <dd>

Der Selektorname. Wenn Sie beispielsweise WMI-Daten anfordern, ist dieser Parameter die Schlüsseleigenschaft für eine WMI-Klasse.

</dd> <dt>

*selValue* \[ In\]
</dt> <dd>

Der Selektorwert. Für WMI-Daten enthält dieser Parameter beispielsweise einen Wert für eine Schlüsseleigenschaft, die eine bestimmte Instanz identifiziert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**IWSManResourceLocator::AddSelector** ist die entsprechende C++-Methode.

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

 

 





