---
description: Die ITablet3-Schnittstelle ermöglicht multifingerabfragen für Eingaben.
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: ITablet3-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f37d70888ccedf0fe941f0387c064aba37dc287e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360816"
---
# <a name="itablet3-interface"></a>ITablet3-Schnittstelle

Die ITablet3-Schnittstelle ermöglicht multifingerabfragen für Eingaben.

## <a name="members"></a>Member

Die **ITablet3** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ITablet3** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITablet3** -Schnittstelle verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**Getmaximumcursors**](itablet3-getmaximumcursors.md) | Ruft die maximal unterstützte Anzahl von Eingaben ab.<br/>        |
| [**ismultiberühren**](itablet3-ismultitouch.md)           | Gibt an, ob multiberühren für dieses Objekt aktiviert ist.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Entwickler sollten diese Schnittstelle nicht verwenden.

Im folgenden Code wird beschrieben, wie die **ITablet3** -Schnittstelle definiert wird.

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

