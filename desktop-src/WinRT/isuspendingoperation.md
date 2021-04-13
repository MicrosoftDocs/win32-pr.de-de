---
description: Enthält Informationen über eine APP, die den Vorgang angehalten.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Isuspendingoperation-Schnittstelle (Windows. applicationmodel. h)
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
ms.openlocfilehash: 09a3c37216298fa672cdd676e835454b4e0f4bd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526222"
---
# <a name="isuspendingoperation-interface"></a>Isuspendingoperation-Schnittstelle

Enthält Informationen über eine APP, die den Vorgang angehalten.

## <a name="members"></a>Member

Die **isuspendingoperation** -Schnittstelle erbt von [**iinspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **Isuspendingoperation** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **isuspendingoperation** -Schnittstelle verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**GetDeferral**](isuspendingoperation-getdeferral.md) | Fordert an, dass der Vorgang zum Anhalten der APP verzögert wird.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **isuspendingoperation** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                     | Zugriffstyp           | BESCHREIBUNG                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [**Stichtag**](isuspendingoperation-deadline.md)<br/> | Lesen/Schreiben<br/> | Ruft die verbleibende Zeit ab, bevor eine verzögerte App angehalten wird.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Header<br/>                   | <dl> <dt>Windows. applicationmodel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. applicationmodel. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**Isuspendingdeferral**](isuspendingdeferral.md)
</dt> <dt>

[**Isuspendingeventargs**](isuspendingeventargs.md)
</dt> </dl>

 

 
