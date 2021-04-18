---
title: IReferenceClock-Schnittstelle
description: Die IReferenceClock-Schnittstelle ermöglicht den Zugriff auf eine externe Uhr. Diese Schnittstelle wird bereitgestellt, um zu ermöglichen, dass alle renderingroutinen mit derselben Uhr synchronisiert werden. Diese Schnittstelle kann von einem Reader-Objekt abgerufen werden.
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- IReferenceClock-Schnittstelle Windows Media-Format
- IReferenceClock-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IReferenceClock
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72d17ef362aa5436fe98443d86dff5ae31212650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338262"
---
# <a name="ireferenceclock-interface"></a>IReferenceClock-Schnittstelle

Die **IReferenceClock** -Schnittstelle ermöglicht den Zugriff auf eine externe Uhr. Diese Schnittstelle wird bereitgestellt, um zu ermöglichen, dass alle renderingroutinen mit derselben Uhr synchronisiert werden.

Diese Schnittstelle kann von einem Reader-Objekt abgerufen werden.

## <a name="members"></a>Member

Die **IReferenceClock** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IReferenceClock** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IReferenceClock** -Schnittstelle verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [**Empfehlungen regelmäßig**](ireferenceclock-adviseperiodic.md) | Wird von diesem SDK nicht implementiert.<br/>                                   |
| [**Empfehlungen**](ireferenceclock-advisetime.md)         | Fordert eine asynchrone Benachrichtigung an, dass eine Zeit abgelaufen ist.<br/> |
| [**GetTime**](ireferenceclock-gettime.md)               | Ruft den aktuellen Verweis Zeitpunkt ab.<br/>                          |
| [**Unadvise**](ireferenceclock-unadvise.md)             | Bricht eine Benachrichtigungs Anforderung ab.<br/>                                |



 

## <a name="remarks"></a>Bemerkungen

Informationen zu anderen Schnittstellen, die mithilfe der QueryInterface-Methode dieser Schnittstelle abgerufen werden können, finden Sie unter Reader-Objekt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](interfaces.md)
</dt> </dl>

 

