---
title: ResourceLocator.MustUnderstandOptions-Eigenschaft (WSManDisp.h)
description: Ruft den MustUnderstandOptions-Wert für das ResourceLocator-Objekt ab oder legt den Wert fest.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- MustUnderstandOptions-Eigenschaft Windows Remoteverwaltung
- MustUnderstandOptions-Eigenschaft Windows Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows Remoteverwaltung , MustUnderstandOptions-Eigenschaft
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
ms.openlocfilehash: a49c3af0372553c221dae902a5fdca0e026bb874f612b8e21f41e6a6870f7ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323738"
---
# <a name="resourcelocatormustunderstandoptions-property"></a>ResourceLocator.MustUnderstandOptions-Eigenschaft

Ruft den **MustUnderstandOptions-Wert** für das [**ResourceLocator-Objekt**](resourcelocator.md) ab oder legt den Wert fest. Sie können ein [**ResourceLocator-Objekt**](resourcelocator.md) angeben, anstatt einen Ressourcen-URI in [**Sitzungsobjektvorgängen**](session.md) wie [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)oder [**Session.Enumerate**](session-enumerate.md)anzugeben.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a>Eigenschaftswert

Gibt bei **True** an, dass der Dienst, der die [WS-Management-Protokoll](ws-management-protocol.md) implementiert, einen Fehler zurückgeben muss, wenn er die Option nicht verarbeiten kann.

## <a name="remarks"></a>Hinweise

**IWSManResourceLocator::MustUnderstandOptions** ist die entsprechende C++-Eigenschaft.

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

 

 





