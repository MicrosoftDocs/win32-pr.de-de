---
description: Die Datentypen für Protected Storage-Methoden.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: PStore-Typen (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6def89ea4beb5d27a98cb8e6f44fc12271de7d1642b236f31f4979ed26b54a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538450"
---
# <a name="pstore-types"></a>PStore-Typen

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Die Datentypen für Protected Storage-Methoden.


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

**PST \_ ACCESSMODE**
</dt> <dd>

Definiert den Lese- oder Schreibmodus der Zugriffsregel.

</dd> <dt>

**PST \_ ACCESSCLAUSETYPE**
</dt> <dd>

Definiert den Klauseltyp der Zugriffsregel.

</dd> <dt>

**\_PST-SCHLÜSSEL**
</dt> <dd>

Definiert den Schlüssel für das gespeicherte Element.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl> |



 

 
