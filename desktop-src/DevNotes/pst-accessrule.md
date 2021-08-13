---
description: Beschreibt eine Regel für den Zugriff auf Elemente, die in geschütztem Speicher gespeichert sind.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: PST_ACCESSRULE-Struktur (Pstore.h)
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
ms.openlocfilehash: 26b4df38c5e5599c13cc52a75c58ea019d786eaa971c8ac3a67a7a8c15651075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667056"
---
# <a name="pst_accessrule-structure"></a>PST \_ ACCESSRULE-Struktur

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, ist in nachfolgenden Versionen jedoch möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den verstärkten Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Beschreibt eine Regel für den Zugriff auf Elemente, die in geschütztem Speicher gespeichert sind.

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

**cbSize**
</dt> <dd>

Die Größe dieser Struktur.

</dd> <dt>

**AccessModeFlags**
</dt> <dd>

Die Zugriffsmodi, für die ein angegebener Satz von Zugriffsklauseln gilt.



| Wert                                                                                                                                                                                                         | Bedeutung                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**PST \_ READ**</dt> <dt>0x0001</dt> </dl>    | Lesezugriffsmodus.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**PST \_ WRITE**</dt> <dt>0x0002</dt> </dl> | Schreibzugriffsmodus.<br/> |



 

</dd> <dt>

**cClauses**
</dt> <dd>

Die Anzahl der Strukturen im **rgClauses-Array.**

</dd> <dt>

**rgClauses**
</dt> <dd>

Ein Zeiger auf ein Array von [**PST \_ ACCESSCLAUSE-Strukturen.**](pst-accessclause.md)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PST \_ ACCESSCLAUSE**](pst-accessclause.md)
</dt> <dt>

[**PST \_ ACCESSRULESET**](pst-accessruleset.md)
</dt> </dl>

 

 
