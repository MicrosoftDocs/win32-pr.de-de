---
description: 'Der LSA- \_ \_ enumerationshandlerdatentyp wird von der LSA-Funktion verwendet, die die Treuhänder-Domänen Objekte auflistet: lsaenumeratetrusteddomainsex.'
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: LSA_ENUMERATION_HANDLE (ntabcapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348639"
---
# <a name="lsa_enumeration_handle"></a>LSA- \_ \_ enumerationshandle

Der **LSA-enumerationshandlerdatentyp \_ \_** wird von der LSA-Funktion verwendet, die die [**Treuhänder-Domänen**](trusteddomain-object.md) Objekte auflistet: [**lsaenumeratetrusteddomainsex**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex). Diese Funktion ist so konzipiert, dass Sie mehrere Aufrufe zum Auflisten aller Objekte eines bestimmten Typs in der Datenbank durchführen können.

Beim anfänglichen enumerationsfunktions-Befehl übergeben Sie einen Zeiger auf eine **LSA- \_ enumerationshandle \_** -Variable, die mit 0 (null) initialisiert wird. Die-Funktion aktualisiert diesen Wert. Wenn die Funktion einen Wert zurückgibt, der angibt, dass weitere Aufzählungs Objekte vorhanden sind, rufen Sie die Funktion erneut auf, und übergeben Sie den aktualisierten **LSA- \_ enumerationshandle \_** -Wert, um eine Enumeration abzurufen, die an dem Punkt fortgesetzt wird, an dem die vorherige Enumeration


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntabcapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Lsaenumeratetrusteddomainsex**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 




