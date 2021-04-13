---
title: Enumerationskonstanten (WSManDisp. h)
description: Die Enumeration enthält Konstanten, wie in der folgenden Liste aufgelistet, die im flags-Parameter durch Aufrufe von Session. Enumerate und iwsmansession Enumerate verwendet werden.
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
ms.openlocfilehash: e422f688fea992ee2d9b1d0d25af00a1d24ad798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391716"
---
# <a name="enumeration-constants"></a>Enumerationskonstanten

Die **\_ \_ wsmanenumflags** -Enumeration enthält Konstanten, wie in der folgenden Liste aufgelistet, die im *Flags* -Parameter durch Aufrufe von [**Session. Enumerate**](session-enumerate.md) und [**iwsmansession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)verwendet werden.

Beachten Sie, dass **wsmanflagreturnobject** und **wsmanflaghierarchydeep** der Standardwert sind, wenn der *Flags* -Parameter nicht angegeben ist.

<dl> <dt>

<span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**Wsmanflagreturnobject**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Batches enthalten die angeforderten XML-Instanzen. Dies ist der Standardwert für den Flag-Parameter.

Die zugeordnete Skript Methode lautet " [**WSMAN. enumerationflagreturnobject**](wsman-enumerationflagreturnobject.md) ", und die C++-Methode ist " [**iwsmanex. enumerationflagreturnobject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject)".


</dt> </dl> </dd> <dt>

<span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**Wsmanflagnonxmltext**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Dieses Flag steuert, wie der *Filter* -Parameter im Aufrufen von [**Session. Enumerate**](session-enumerate.md) von WinRM interpretiert wird.

Das Format des Filters kann ein XML-Fragment oder eine Text Zeichenfolge sein. Das Format wird durch den [*Filter Dialekt*](windows-remote-management-glossary.md) des [*Filters*](windows-remote-management-glossary.md) bestimmt, der im Aufrufen von [**Session. Enumerate**](session-enumerate.md) oder [**iwsmansession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)verwendet wird, der spezifisch für den ausgeführten Vorgang ist.

Wenn der *Dialekt* Parameter nicht angegeben wird, versucht WinRM, den Dialekt basierend auf dem ersten Zeichen des Filters zu ermitteln. Wenn das erste Zeichen < ist, der Filter jedoch nicht tatsächlich ein XML-Fragment ist, sollte dieses Flag festgelegt werden. Ein Filter im folgenden Format erfordert beispielsweise, dass Sie **wsmanflagnonxmltext** festlegen, damit der Filter ordnungsgemäß interpretiert wird:

`<25 && > 1`

Wenn der Filter ein XML-Fragment ist, ist dieses Flag nicht erforderlich, da das Fragment mit < beginnt, das WinRM ordnungsgemäß als XML interpretiert. Beispiel:

`<filter>select * from aDataStructure</filter>`

Wenn sich der Filter im nur-Text-Modus befindet, der nicht mit < beginnt, ist dieses Flag nicht erforderlich. Beispiel:

`select * from aDataStructure`

Die zugeordnete Skript Methode ist [**WSMAN. enumerationflagnonxmltext**](wsman-enumerationflagnonxmltext.md) , und die C++-Methode ist [**iwsmanex. enumerationflagnonxmltext**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).


</dt> </dl> </dd> <dt>

<span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**Enumerationflagreturnetpr**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Batches enthalten Endpunkt Verweise (EPRS) für die entsprechenden XML-Instanzen, jedoch nicht die eigentlichen Instanzen.

Die zugeordnete Skript Methode ist [**WSMAN. enumerationflagreturnetpr**](wsman-enumerationflagreturnepr.md) , und die C++-Methode ist [**iwsmanex. enumerationflagreturnetpr**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).


</dt> </dl> </dd> <dt>

<span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**Wsmanflagreturnobjectandepr**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Batches enthalten sowohl die angeforderte XML-Instanz als auch die entsprechenden EPRS, die in einem [*WSMAN: Items*](windows-remote-management-glossary.md) -Element enthalten sind.

Die zugeordnete Skript Methode lautet " [**WSMAN. enumerationflagreturnobjectandepr**](wsman-enumerationflagreturnobjectandepr.md) ", und die C++-Methode ist " [**iwsmanex. enumerationflagreturnobjectandepr**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr)".


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**Wsmanflaghierarchydeep**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Abgeleitete Klassen Instanzen werden eingeschlossen und entsprechend ihren eigentlichen Schemas dargestellt.

Die zugeordnete Skript Methode lautet [**WSMAN. enumerationflaghierarchydeep**](wsman-enumerationflaghierarchydeep.md) und die C++-Methode ist [**iwsmanex. enumerationflaghierarchydeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**Wsmanflaghierarchyflache**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Abgeleitete Klassen Instanzen werden ausgeschlossen. Es werden nur Instanzen des angeforderten Typs angezeigt.

Die zugeordnete Skript Methode ist [**WSMAN. enumerationflaghierarchyflache**](wsman-enumerationflaghierarchyshallow.md) , und die C++-Methode ist [**iwsmanex. enumerationflaghierarchyflache**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**Wsmanflaghierarchydeepbasepropsonly**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Abgeleitete Klassen Instanzen werden eingeschlossen und entsprechend dem Basisklassen Schema dargestellt. Eigenschaften, die in der abgeleiteten Klasse definiert sind, werden nicht angezeigt.

Die zugeordnete Skript Methode lautet [**WSMAN. enumerationflaghierarchydeepbasepropsonly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) , und die C++-Methode ist [**iwsmanex. enumerationflaghierarchydeepbasepropsonly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WinRM-Konstanten und-Enumerationen](winrm-constants-and-enumerations.md)
</dt> <dt>

[Auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Abfragen für bestimmte Instanzen einer Ressource](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





