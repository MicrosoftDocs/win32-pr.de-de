---
description: Die "ikspin"-Schnittstelle bietet eine Methode zum Abrufen der von einer PIN in einem kernelmodusfilter unterstützten Medien. "Ikspin" hat neben dem hier gezeigten zusätzliche Methoden, aber Sie werden für DirectShow nicht unterstützt.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Ikspin-Schnittstelle (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 3d65e5ba5525b977ebae27da9964579614a1d653
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345401"
---
# <a name="ikspin-interface"></a>Ikspin-Schnittstelle

Die `IKsPin` -Schnittstelle stellt eine Methode zum Abrufen der von einer PIN in einem Kernel Modus-Filter unterstützten Medien bereit. `IKsPin` hat neben dem hier gezeigten zusätzliche Methoden, aber Sie werden für DirectShow nicht unterstützt.

## <a name="members"></a>Member

Die " **ikspin** "-Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. In " **ikspin** " sind auch folgende Typen von Membern aufgeführt:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ikspin** -Schnittstelle verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [**Ksquerymediums**](ikspin-ksquerymediums.md) | Ruft die von einer PIN unterstützten Medien ab.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Sie müssen "KS. h" vor "ksproxy. h" einschließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Bibliothek<br/>                  | <dl> <dt>"" "" ". Lib"</dt> </dl> |



 

 
