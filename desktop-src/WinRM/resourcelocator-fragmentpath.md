---
title: ResourceLocator.FragmentPath-Eigenschaft (WSManDisp.h)
description: Ruft den Pfad für ein Ressourcenfragment oder eine Eigenschaft ab, wenn ResourceLocator in Sitzungsobjektvorgängen wie Session.Get, Session.Put oder Session.Enumerate verwendet wird, oder legt diesen fest.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- FragmentPath-Eigenschaft Windows Remoteverwaltung
- FragmentPath-Eigenschaft Windows Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows Remoteverwaltung, FragmentPath-Eigenschaft
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f756d669ba79ce034a9562d6cae5d58653bc60e042344306fb18aa37edfdc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121630"
---
# <a name="resourcelocatorfragmentpath-property"></a>ResourceLocator.FragmentPath (Eigenschaft)

Ruft den Pfad für [](windows-remote-management-glossary.md) [](windows-remote-management-glossary.md) ein Ressourcenfragment oder eine Eigenschaft ab, wenn [**ResourceLocator**](resourcelocator.md) [**in**](session.md) Sitzungsobjektvorgängen wie [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)oder [**Session.Enumerate**](session-enumerate.md)verwendet wird, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die das Fragment oder die Eigenschaft der Ressource identifiziert. Wenn die Ressource beispielsweise ein Laufwerk und die angeforderte Eigenschaft Manufacturer ist, kann die Zeichenfolge `Diskdrive/Manufacturer` enthalten. Beim Fragmenttext wird die Kleinschreibung beachtet. In diesem Fall können Sie nicht `diskdrive/manufacturer` verwenden.

## <a name="remarks"></a>Hinweise

**IWSManResourceLocator::FragmentPath** ist die entsprechende C++-Eigenschaft.

Sie können ein Element einer Arrayeigenschaft angeben, indem Sie den Arrayindex wie im folgenden Beispiel gezeigt angeben. Beachten Sie, dass die Arrayindizierung mit 1 anstatt mit 0 beginnt.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



Um das gesamte Array zu erhalten, geben Sie den Arrayeigenschaftsnamen an, wie im folgenden Beispiel gezeigt.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



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

 

 





