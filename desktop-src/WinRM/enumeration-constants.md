---
title: Enumerationskonst constants (WSManDisp.h)
description: Enumeration enthält Konstanten, wie in der folgenden Liste aufgeführt, die im flags-Parameter durch Aufrufe von Session.Enumerate und IWSManSession Enumerate verwendet werden.
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c8182352d2ebf3763a38f74dd6f100dc836e88cfa10212ffaa971048ebd1aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113262"
---
# <a name="enumeration-constants"></a>Enumerationskonst constants

Die **\_ \_ WSManEnumFlags-Enumeration** enthält Konstanten, wie in der folgenden Liste aufgeführt, die im *flags-Parameter* durch Aufrufe von [**Session.Enumerate**](session-enumerate.md) und [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)verwendet werden.

Beachten Sie, dass **WSManFlagReturnObject** und **WSManFlagHierarchyDeep** die Standardeinstellung sind, wenn der *flags-Parameter* nicht angegeben ist.

<dl> <dt>

<span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Batches enthalten die angeforderten XML-Instanzen. Dies ist der Standardwert für den Flagparameter.

Die zugeordnete Skriptmethode ist [**WSMan.EnumerationFlagReturnObject,**](wsman-enumerationflagreturnobject.md) und die C++-Methode [**ist IWSManEx.EnumerationFlagReturnObject.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject)


</dt> </dl> </dd> <dt>

<span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Dieses Flag steuert, wie *der Filterparameter* im Aufruf von [**Session.Enumerate**](session-enumerate.md) von WinRM interpretiert wird.

Das Format des Filters kann ein XML-Fragment oder eine Zeichenfolge mit Nur-Text sein. Das Format wird [](windows-remote-management-glossary.md) durch den [](windows-remote-management-glossary.md) Filterdialekt des Filters bestimmt, der im Aufruf von [**Session.Enumerate**](session-enumerate.md) oder [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)verwendet wird, der für den ausgeführten Vorgang spezifisch ist.

Wenn der *Dialektparameter* nicht angegeben ist, versucht WinRM, den Dialekt basierend auf dem ersten Zeichen des Filters zu bestimmen. Wenn das erste Zeichen < ist, der Filter jedoch kein XML-Fragment ist, sollte dieses Flag festgelegt werden. Beispielsweise erfordert ein Filter im folgenden Format, dass **Sie WSManFlagNonXmlText** so festlegen, dass der Filter ordnungsgemäß interpretiert wird:

`<25 && > 1`

Wenn der Filter ein XML-Fragment ist, ist dieses Flag nicht erforderlich, da das Fragment mit < beginnt, die WinRM ordnungsgemäß als XML interpretiert. Beispiel:

`<filter>select * from aDataStructure</filter>`

Wenn sich der Filter im Nur-Text-Text befindet, der nicht mit < beginnt, ist dieses Flag nicht erforderlich. Beispiel:

`select * from aDataStructure`

Die zugeordnete Skriptmethode ist [**WSMan.EnumerationFlagNonXmlText,**](wsman-enumerationflagnonxmltext.md) und die C++-Methode [**ist IWSManEx.EnumerationFlagNonXmlText.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext)


</dt> </dl> </dd> <dt>

<span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Batches enthalten Endpunktverweise (EPRs) für die entsprechenden XML-Instanzen, aber nicht die tatsächlichen Instanzen.

Die zugeordnete Skriptmethode ist [**WSMan.EnumerationFlagReturnEPR,**](wsman-enumerationflagreturnepr.md) und die C++-Methode [**ist IWSManEx.EnumerationFlagReturnEPR.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr)


</dt> </dl> </dd> <dt>

<span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Batches enthalten sowohl die angeforderten XML-Instanzen als auch die entsprechenden EPRs, die in einem [*wsman:Items-Element enthalten*](windows-remote-management-glossary.md) sind.

Die zugeordnete Skriptmethode ist [**WSMan.EnumerationFlagReturnObjectAndEPR,**](wsman-enumerationflagreturnobjectandepr.md) und die C++-Methode [**ist IWSManEx.EnumerationFlagReturnObjectAndEPR.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr)


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Abgeleitete Klasseninstanzen sind enthalten und werden entsprechend ihren tatsächlichen Schemas dargestellt.

Die zugeordnete Skriptmethode ist [**WSMan.EnumerationFlagHierarchyDeep,**](wsman-enumerationflaghierarchydeep.md) und die C++-Methode [**ist IWSManEx.EnumerationFlagHierarchyDeep.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep)


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Abgeleitete Klasseninstanzen werden ausgeschlossen. Es werden nur Instanzen des angeforderten Typs angezeigt.

Die zugeordnete Skriptmethode ist [**WSMan.EnumerationFlagHierarchyShallow,**](wsman-enumerationflaghierarchyshallow.md) und die C++-Methode [**ist IWSManEx.EnumerationFlagHierarchyShallow.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow)


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Abgeleitete Klasseninstanzen sind enthalten und werden entsprechend dem Basisklassenschema dargestellt. In der abgeleiteten Klasse definierte Eigenschaften werden nicht angezeigt.

Die zugeordnete Skriptmethode ist [**WSMan.EnumerationFlagHierarchyDeepBasePropsOnly,**](wsman-enumerationflaghierarchydeepbasepropsonly.md) und die C++-Methode [**ist IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly)


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[WinRM-Konstanten und -Enumerationen](winrm-constants-and-enumerations.md)
</dt> <dt>

[Auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Abfragen bestimmter Instanzen einer Ressource](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





