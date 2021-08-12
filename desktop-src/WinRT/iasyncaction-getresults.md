---
description: Ruft das Ergebnis einer asynchronen Aktion ab.
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: IAsyncAction::GetResults-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 62196c7f8ded67bed0ecdb3ea33420de54301bbd379615126ada158ea9e725ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561052"
---
# <a name="iasyncactiongetresults-method"></a>IAsyncAction::GetResults-Methode

Ruft das Ergebnis einer asynchronen Aktion ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResults();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Diese Methode gibt immer **S \_ OK** zurück.

## <a name="remarks"></a>Hinweise

Das Aufrufen der **GetResults-Methode** hat keine Auswirkungen, wenn die aktuelle Implementierung den dynamischen Typ [**IAsyncAction aufweist.**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Windows. Foundation.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
