---
title: ResourceLocator. Fragmentdialekt-Eigenschaft (WSManDisp. h)
description: Ruft den sprach Dialekt für einen Ressourcen Fragment-Dialekt ab, wenn ResourceLocator in Sitzungs Objekt Vorgängen wie "Session. Get", "Session. Put" oder "Session. Enumerate" verwendet wird, oder legt ihn fest.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- Fragmentdialekt-Eigenschaft Windows-Remoteverwaltung
- Fragmentdialekt-Eigenschaft Windows-Remoteverwaltung, ResourceLocator-Objekt
- ResourceLocator-Objekt Windows-Remoteverwaltung, Fragmentdialekt (Eigenschaft)
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
ms.openlocfilehash: f1fe42c2bbe15c75d5f38ea47119f9649e678931
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478783"
---
# <a name="resourcelocatorfragmentdialect-property"></a>ResourceLocator. Fragmentdialekt (Eigenschaft)

Ruft den sprach Dialekt für einen [*Ressourcen*](windows-remote-management-glossary.md) [*Fragment*](windows-remote-management-glossary.md) - *Dialekt* ab, wenn [**ResourceLocator**](resourcelocator.md) in [**Sitzungs**](session.md) Objekt Vorgängen wie " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)" verwendet wird, oder legt ihn fest. Ein Fragment stellt eine Eigenschaft oder einen Teil einer Ressource dar. Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt bereitstellen, anstatt einen Ressourcen-URI in [**Sitzungs**](session.md) Objekt Vorgängen anzugeben. Der Dialekt gibt an, welche XML-Sprache das Fragment für den Dienst beschreibt, der die [WS-Management-Protokoll](ws-management-protocol.md) implementiert und die Anforderung empfängt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a>Eigenschaftswert

Eine XML-Zeichenfolge, die die Sprache angibt, die in der [**fragmentpath**](resourcelocator-fragmentpath.md) -Eigenschaft verwendet wird. Die Dialekt Zeichenfolge ist standardmäßig die XPath 1,0-Spezifikation. Weitere Informationen finden Sie unter [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="remarks"></a>Bemerkungen

[**Iwsmanresourcelocator:: Fragmentdialekt**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) ist die entsprechende C++-Eigenschaft.

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

 

 





