---
description: Ruft das Ergebnis einer asynchronen Aktion ab.
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: 'Iasyncaction:: GetResults-Methode'
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
ms.openlocfilehash: 292c73846227f1bb8884b24b7e709bc6b2296e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214607"
---
# <a name="iasyncactiongetresults-method"></a>Iasyncaction:: GetResults-Methode

Ruft das Ergebnis einer asynchronen Aktion ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetResults();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Diese Methode gibt immer **\_ OK** zurück.

## <a name="remarks"></a>Bemerkungen

Das Aufrufen der **GetResults** -Methode hat keine Auswirkungen, wenn die aktuelle Implementierung einen dynamischen [**iasyncaction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)-Typ aufweist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
