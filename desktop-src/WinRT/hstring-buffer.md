---
description: Ein Handle für einen änderbaren Zeichen folgen Puffer, der zum Erstellen eines hstring verwendet werden kann.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d70b961d442739e084e3b17d5666653c103cc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348185"
---
# <a name="hstring_buffer"></a>hstring- \_ Puffer

Ein Handle für einen änderbaren Zeichen folgen Puffer, der zum Erstellen eines [**hstring**](hstring.md)verwendet werden kann.


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a>Bemerkungen

**Hstring \_ Buffer** stellt einen Zeichen folgen Puffer dar, den Sie ändern können, bevor Sie ihn in einen unveränderlichen [**hstring**](hstring.md)-Wert umrechnen.

Rufen Sie die [**windowshalzugecatestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) -Funktion auf, um einen **hstring- \_ Puffer** zu erstellen. Ruft den [**windowspromotestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) auf, um einen **hstring- \_ Puffer** in einen unveränderlichen [**hstring**](hstring.md)zu konvertieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Header<br/>                   | <dl> <dt>Hstring. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**HSTRING**](hstring.md)
</dt> <dt>

[**Windowshalzugecatestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[**Windowspromotestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
