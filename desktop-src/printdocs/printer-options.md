---
description: Stellt Druckeroptionen dar.
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: PRINTER_OPTIONS Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 37c45277f0a7e30bc94b2d23ffa27de0092a7164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362535"
---
# <a name="printer_options-structure"></a>Struktur der Drucker \_ Optionen

Stellt Druckeroptionen dar.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Die Größe der **Drucker \_ options** Struktur.

</dd> <dt>

**dwFlags**
</dt> <dd>

Ein Satz von [**\_ druckeroptionsflags \_**](printer-option-flags.md) , der angibt, wie das Handle für einen Drucker, der von [**OpenPrinter2**](openprinter2.md) zurückgegeben wird, von anderen Funktionen verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**\_druckeroptionsflags \_**](printer-option-flags.md)
</dt> </dl>

 

 




