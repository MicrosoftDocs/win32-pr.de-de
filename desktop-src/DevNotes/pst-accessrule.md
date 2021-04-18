---
description: Beschreibt eine Regel für den Zugriff auf Elemente, die im geschützten Speicher gespeichert sind.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: PST_ACCESSRULE Struktur (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 90a04f2f7a34874a8c076fa55b158944399fac2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371265"
---
# <a name="pst_accessrule-structure"></a>PST- \_ AccessRule-Struktur

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Beschreibt eine Regel für den Zugriff auf Elemente, die im geschützten Speicher gespeichert sind.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Die Größe dieser Struktur.

</dd> <dt>

**Accessmodeflags**
</dt> <dd>

Die Zugriffs Modi, auf die sich ein angegebener Satz von Zugriffs Klauseln bezieht.



| Wert                                                                                                                                                                                                         | Bedeutung                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**PST \_ Lesen**</dt> von <dt>0x0001</dt> </dl>    | Lese Zugriffsmodus.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**PST \_ Schreiben**</dt> von <dt>0x0002</dt> </dl> | Schreibzugriffs Modus.<br/> |



 

</dd> <dt>

**cklauseln**
</dt> <dd>

Die Anzahl der Strukturen im **rgklauseln** -Array.

</dd> <dt>

**rgklauseln**
</dt> <dd>

Ein Zeiger auf ein Array von [**PST \_ accessclause**](pst-accessclause.md) -Strukturen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PST- \_ accessclause**](pst-accessclause.md)
</dt> <dt>

[**PST- \_ accessruleset**](pst-accessruleset.md)
</dt> </dl>

 

 
