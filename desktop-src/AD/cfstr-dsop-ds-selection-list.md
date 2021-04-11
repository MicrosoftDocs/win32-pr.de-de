---
title: CFSTR_DSOP_DS_SELECTION_LIST (objsel. h)
description: Das Format der cfstr \_ DSOP \_ DS- \_ Auswahlliste in der \_ Zwischenablage bietet einen HGLOBAL, der eine DS- \_ Auswahl \_ Listenstruktur enthält. Die Struktur der DS- \_ Auswahl \_ Liste enthält Daten zu den Elementen, die im Dialogfeld Verzeichnis Objektauswahl ausgewählt wurden.
ms.assetid: cd634e3b-0eb7-4144-b9e1-1d27a322f72c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOP_DS_SELECTION_LIST
api_location:
- Objsel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b783b0790ed87a292cd171cb8283333d5b9bd5b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949717"
---
# <a name="cfstr_dsop_ds_selection_list"></a>cfstr \_ DSOP \_ DS- \_ Auswahl \_ Liste

<dl> <dt>

<span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**cfstr \_ DSOP \_ DS- \_ Auswahl \_ Liste**
</dt> <dd> <dl> <dt>

"cfstr \_ DSOP \_ DS- \_ Auswahl \_ Liste"
</dt> <dt>



Das Zwischenablage Format der **cfstr \_ DSOP \_ DS- \_ Auswahl \_ Liste** wird durch das [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) bereitgestellt, das durch Aufrufen von [**idsobjectpicker:: invokedialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)abgerufen wird. Das Format der **cfstr \_ DSOP \_ DS- \_ Auswahl \_ Liste** in der Zwischenablage bietet einen **HGLOBAL** , der eine [**DS- \_ Auswahl \_ Listen**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) Struktur enthält. Die Struktur der **DS- \_ Auswahl \_ Liste** enthält Daten zu den Elementen, die im Dialogfeld [Verzeichnis Objekt](directory-object-picker.md) Auswahl ausgewählt wurden.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                      |
| Header<br/>                   | <dl> <dt>Objsel. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DS- \_ Auswahl \_ Liste**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)
</dt> <dt>

[**Idsobjectpicker:: invokedialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)
</dt> <dt>

[Verzeichnis Objektauswahl](directory-object-picker.md)
</dt> </dl>

 

