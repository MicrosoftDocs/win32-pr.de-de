---
title: ResourceLocator. mustverständlicherweise Options-Eigenschaft (WSManDisp. h)
description: Ruft den mustverständlicherweise Options-Wert für das ResourceLocator-Objekt ab oder legt ihn fest.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- Mustverständlicherweise Options-Eigenschaft Windows-Remoteverwaltung
- Mustverständlicherweise Options-Eigenschaft Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, mustverständlicherweise Options-Eigenschaft
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2945efd1a224c333f45956a29df779efc98e944f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957051"
---
# <a name="resourcelocatormustunderstandoptions-property"></a>ResourceLocator. mustverständlicherweise Options-Eigenschaft

Ruft den **mustverständlicherweise Options** -Wert für das [**ResourceLocator**](resourcelocator.md) -Objekt ab oder legt ihn fest. Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt bereitstellen, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" anzugeben.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a>Eigenschaftswert

Gibt an, dass der Dienst, der die [WS-Management-Protokoll](ws-management-protocol.md) implementiert, beim Wert " **true**" einen Fehler zurückgeben muss, wenn er die Option nicht verarbeiten kann.

## <a name="remarks"></a>Bemerkungen

**Iwsmanresourcelocator:: mustverständlicherweise Options** ist die entsprechende C++-Eigenschaft.

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

 

 





