---
description: Gibt den Satz von Zugriffsregeln für die geschützten Speicherdaten an.
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: PST_ACCESSRULESET Struktur (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: b4c339ea0866ad872d5d0a2f8eaff6be947adc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371689"
---
# <a name="pst_accessruleset-structure"></a>PST- \_ accessruleset-Struktur

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Gibt den Satz von Zugriffsregeln für die geschützten Speicherdaten an.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Die Größe dieser Struktur.

</dd> <dt>

**crules**
</dt> <dd>

Die Anzahl der Regeln im **rgrules** -Array.

</dd> <dt>

**rgrules**
</dt> <dd>

Ein Zeiger auf ein Array von [**PST- \_ AccessRule**](pst-accessrule.md) -Strukturen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PST- \_ AccessRule**](pst-accessrule.md)
</dt> <dt>

[**"Kreatesubtype"**](ipstore-createsubtype.md)
</dt> </dl>

 

 
