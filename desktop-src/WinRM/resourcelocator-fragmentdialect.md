---
title: ResourceLocator.FragmentDialect-Eigenschaft (WSManDisp.h)
description: Ruft den Sprachdialekt für einen Ressourcenfragmentdialekt ab, wenn ResourceLocator in Sitzungsobjektvorgängen wie Session.Get, Session.Put oder Session.Enumerate verwendet wird, oder legt diesen fest.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- FragmentDialect-Eigenschaft Windows Remoteverwaltung
- FragmentDialect-Eigenschaft Windows Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows Remoteverwaltung, FragmentDialect-Eigenschaft
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ae7cbbd71b4ccad24ecaa17d0fd635761f661bcd6dc95ebc0345e9164adcd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997300"
---
# <a name="resourcelocatorfragmentdialect-property"></a>ResourceLocator.FragmentDialect-Eigenschaft

Ruft den Sprachdialekt für einen [](windows-remote-management-glossary.md) [*Ressourcenfragmentdialekt*](windows-remote-management-glossary.md)  ab, wenn [**ResourceLocator**](resourcelocator.md) in [**Sitzungsobjektvorgängen**](session.md) wie [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)oder [**Session.Enumerate**](session-enumerate.md)verwendet wird, oder legt diesen fest. Ein Fragment stellt eine Eigenschaft oder einen Teil einer Ressource dar. Sie können ein [**ResourceLocator-Objekt**](resourcelocator.md) angeben, anstatt einen Ressourcen-URI in [**Sitzungsobjektvorgängen**](session.md) anzugeben. Der Dialekt gibt an, welche XML-Sprache das Fragment für den Dienst beschreibt, der die [WS-Management-Protokoll](ws-management-protocol.md) implementiert und die Anforderung empfängt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a>Eigenschaftswert

Eine XML-Zeichenfolge, die die in der [**FragmentPath-Eigenschaft**](resourcelocator-fragmentpath.md) verwendete Sprache identifiziert. Die Dialektzeichenfolge verwendet standardmäßig die XPath 1.0-Spezifikation. Weitere Informationen finden Sie unter [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="remarks"></a>Hinweise

[**IWSManResourceLocator::FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) ist die entsprechende C++-Eigenschaft.

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

 

 





