---
description: Stellt Informationen zu einem Vorgang zum Anhalten einer App bereit.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: ISuspendingOperation-Schnittstelle (Windows. ApplicationModel.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: f17cd3d3b1eab67d0abfea200e657d8c4a17d8df9e3bb850e4ea361a760d19df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758630"
---
# <a name="isuspendingoperation-interface"></a>ISuspendingOperation-Schnittstelle

Stellt Informationen zu einem Vorgang zum Anhalten einer App bereit.

## <a name="members"></a>Member

Die **ISuspendingOperation-Schnittstelle** erbt von [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingOperation** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ISuspendingOperation-Schnittstelle** verfügt über diese Methoden.



| Methode                                                  | Beschreibung                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**GetDeferral**](isuspendingoperation-getdeferral.md) | Fordert an, dass der Vorgang zum Anhalten der App verzögert wird.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **ISuspendingOperation-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                     | Zugriffstyp           | Beschreibung                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [**Stichtag**](isuspendingoperation-deadline.md)<br/> | Lesen/Schreiben<br/> | Ruft die verbleibende Zeit ab, bevor ein verzögerter App-Unterbrechungsvorgang fortgesetzt wird.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Windows. ApplicationModel.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> </dl>

 

 
