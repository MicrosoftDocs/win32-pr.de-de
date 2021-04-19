---
description: Verwaltet einen verzögerten Vorgang zum Anhalten der app.
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: Isuspendingdeferral-Schnittstelle (Windows. applicationmodel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348184"
---
# <a name="isuspendingdeferral-interface"></a>Isuspendingdeferral-Schnittstelle

Verwaltet einen verzögerten Vorgang zum Anhalten der app.

## <a name="members"></a>Member

Die **isuspendingdeferral** -Schnittstelle erbt von [**iinspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **Isuspendingdeferral** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **isuspendingdeferral** -Schnittstelle verfügt über diese Methoden.



| Methode                                           | BESCHREIBUNG                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Abgeschlossen**](isuspendingdeferral-complete.md) | Benachrichtigt das System, dass die APP Ihre Daten gespeichert hat und bereit ist, angehalten zu werden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>Windows. applicationmodel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. applicationmodel. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**Isuspendingeventargs**](isuspendingeventargs.md)
</dt> <dt>

[**Isuspendingoperation**](isuspendingoperation.md)
</dt> </dl>

 

 
