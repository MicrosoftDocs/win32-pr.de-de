---
description: Enthält Informationen zur Zugriffsklausel für den geschützten Speicher.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: PST_ACCESSCLAUSE-Struktur (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: e5933b762ac19ac188e2d7253e86482caae968abd58ecb02087c32657d250216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386180"
---
# <a name="pst_accessclause-structure"></a>PST \_ ACCESSCLAUSE-Struktur

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Enthält Informationen zur Zugriffsklausel für den geschützten Speicher.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a>Member

<dl> <dt>

**cbSize**
</dt> <dd>

Die Größe dieser Struktur.

</dd> <dt>

**ClauseType**
</dt> <dd>

Der Datentyp, auf den der **pbClauseData-Member** zeigt. Weitere Informationen finden Sie unter [**PStore-Typen.**](pstore-types.md)

</dd> <dt>

**cbClauseData**
</dt> <dd>

Die Größe der Daten, auf die der **pbClauseData-Member** zeigt.

</dd> <dt>

**pbClauseData**
</dt> <dd>

Ein Zeiger auf die Daten der Zugriffsklausel.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PST \_ ACCESSRULE**](pst-accessrule.md)
</dt> </dl>

 

 
