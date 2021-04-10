---
title: ResourceLocator. fragmentpath-Eigenschaft (WSManDisp. h)
description: Ruft den Pfad für ein Ressourcen Fragment oder eine Ressourcen Eigenschaft ab oder legt diesen fest, wenn ResourceLocator in Sitzungs Objekt Vorgängen verwendet wird, z. b. Session. Get, Session. Put oder Session. Enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- Fragmentpath-Eigenschaft Windows-Remoteverwaltung
- Fragmentpath-Eigenschaft Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, fragmentpath-Eigenschaft
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
ms.openlocfilehash: e15fba102f9a7c8a2581271c575857b49bc5df1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040647"
---
# <a name="resourcelocatorfragmentpath-property"></a>ResourceLocator. fragmentpath (Eigenschaft)

Ruft den Pfad für ein [*Ressourcen*](windows-remote-management-glossary.md) [*Fragment*](windows-remote-management-glossary.md) oder eine Ressourcen Eigenschaft ab oder legt diesen fest, wenn [**ResourceLocator**](resourcelocator.md) in [**Sitzungs**](session.md) Objekt Vorgängen verwendet wird, z. b [**. Session. Get**](session-get.md), [**Session. Put**](session-put.md)oder [**Session. Enumerate**](session-enumerate.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zeichenfolge, die das Fragment oder die Eigenschaft der Ressource identifiziert. Wenn die Ressource z. b. ein Laufwerk ist und die angeforderte Eigenschaft Hersteller ist, kann die Zeichenfolge enthalten `Diskdrive/Manufacturer` . Beim Fragmenttext wird Groß-/Kleinschreibung beachtet. In diesem Fall können Sie nicht verwenden `diskdrive/manufacturer` .

## <a name="remarks"></a>Bemerkungen

**Iwsmanresourcelocator:: fragmentpath** ist die entsprechende C++-Eigenschaft.

Sie können ein Element einer Array Eigenschaft angeben, indem Sie den Array Index bereitstellen, wie im folgenden Beispiel gezeigt. Beachten Sie, dass die Array Indizierung mit 1 statt 0 beginnt.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



Um das gesamte Array zu erhalten, geben Sie den Namen der Array Eigenschaft an, wie im folgenden Beispiel gezeigt.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





