---
description: Enthält Informationen über die Access-Klausel für den geschützten Speicher.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: PST_ACCESSCLAUSE Struktur (pstore. h)
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
ms.openlocfilehash: 3536b92bf1d014090f124976b8f4a16e25beb444
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366897"
---
# <a name="pst_accessclause-structure"></a>PST \_ accessclause-Struktur

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Enthält Informationen über die Access-Klausel für den geschützten Speicher.

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

**CBSIZE**
</dt> <dd>

Die Größe dieser Struktur.

</dd> <dt>

**Klsie Type**
</dt> <dd>

Der Typ der Daten, auf die vom **pbclau-Data** -Member verwiesen wird. Weitere Informationen finden Sie unter [**pstore-Typen**](pstore-types.md).

</dd> <dt>

**cbclauabdata**
</dt> <dd>

Die Größe der Daten, auf die vom **pbclau-Data** -Member verwiesen wird.

</dd> <dt>

**pbclauabdata**
</dt> <dd>

Ein Zeiger auf die Daten der Access-Klausel.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PST- \_ AccessRule**](pst-accessrule.md)
</dt> </dl>

 

 
