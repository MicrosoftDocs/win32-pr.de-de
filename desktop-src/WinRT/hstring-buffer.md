---
description: Ein Handle für einen veränderlichen Zeichenfolgenpuffer, den Sie zum Erstellen eines HSTRING verwenden können.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (Hstring.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f115ca18b4bf5b81bbd7004259aa525517c05a3adc0f6376f7d16df3e3ce679
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733820"
---
# <a name="hstring_buffer"></a>HSTRING \_ BUFFER

Ein Handle für einen änderbaren Zeichenfolgenpuffer, mit dem Sie einen [**HSTRING**](hstring.md)erstellen können.


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a>Hinweise

**HSTRING \_ BUFFER** stellt einen Zeichenfolgenpuffer dar, den Sie ändern können, bevor Sie ihn in einen unveränderlichen [**HSTRING**](hstring.md)konvertieren.

Rufen Sie die [**WindowsPreallocateStringBuffer-Funktion**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) auf, um einen **HSTRING \_ BUFFER** zu erstellen. Rufen Sie [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) auf, um einen **HSTRING \_ BUFFER** in einen unveränderlichen [**HSTRING**](hstring.md)zu konvertieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Header<br/>                   | <dl> <dt>Hstring.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**HSTRING**](hstring.md)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
