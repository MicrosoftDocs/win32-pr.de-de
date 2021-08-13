---
description: Tritt ein, wenn Windows Store App aktiviert wird.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: ICoreApplicationView::Activated-Ereignis (Windows. ApplicationModel.Core.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e736d0fb5403fe76d6d402c261e6b7e5336dfc096d8c39d7b3300b93ab1332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560994"
---
# <a name="icoreapplicationviewactivated-event"></a>ICoreApplicationView::Activated-Ereignis

Tritt ein, wenn Windows Store App aktiviert wird.

## <a name="syntax"></a>Syntax


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handler* \[ In\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Rufen Sie die [**Exit-Methode nicht**](/previous-versions//hh438368(v=vs.85)) innerhalb des Handlers *auf.*

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                               |
| Header<br/>                   | <dl> <dt>Windows. ApplicationModel.Core.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Windows. ApplicationModel.Core.idl</dt> </dl> |



 

 
