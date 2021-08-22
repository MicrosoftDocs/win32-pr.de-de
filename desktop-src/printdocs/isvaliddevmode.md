---
description: Die IsValidDevmode-Funktion überprüft, ob der Inhalt einer DEVMODE-Struktur gültig ist.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: IsValidDevmode-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4c3a5cd33a6a5584ea9373df22df51a09e3e763d284a0f979f0b24e3651dc3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100528"
---
# <a name="isvaliddevmode-function"></a>IsValidDevmode-Funktion

Die **IsValidDevmode-Funktion** überprüft, ob der Inhalt einer DEVMODE-Struktur gültig ist.

## <a name="syntax"></a>Syntax


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevmode* \[ In\]
</dt> <dd>

Ein Zeiger auf den [**zu überprüfenden DEVMODE.**](/windows/win32/api/wingdi/ns-wingdi-devmodea)

</dd> <dt>

*DevmodeSize* 
</dt> <dd>

Die Größe des Eingabebytepuffers in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**TRUE**, wenn [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) strukturell gültig ist. Wenn kleinere Fehler gefunden werden, werden sie von der Funktion behoben und **TRUE zurückgeben.**

**FALSE**, wenn [**DEVMODE ein**](/windows/win32/api/wingdi/ns-wingdi-devmodea) oder mehrere signifikante strukturelle Probleme aufthält. Beispielsweise ist der **dmSize-Member** falsch ausgerichtet oder gibt einen puffer an, der zu klein ist. False, **wenn** **pDevmode** NULL **ist.**

## <a name="remarks"></a>Hinweise

Es werden keine privaten Druckertreiberfelder von [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) überprüft, sondern nur die öffentlichen Felder.

Aufrufer sollten **dmSize** + **dmDriverExtra** nur für **DevmodeSize** verwenden, wenn sie garantieren können, dass die Eingabepuffergröße mindestens so groß ist. Da [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) im Allgemeinen nicht vertrauenswürdige Daten sind, sind die Werte im Eingabepuffer am **dmSize-** und **dmDriverExtra-Offset** ebenfalls nicht vertrauenswürdig.

Diese Funktion ist im Kontext Least-Privileged Benutzerkontos (USER Account, LUA) ausführbare Datei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Winspool.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **IsValidDevmodeW** (Unicode) und **IsValidDevmodeA** (ANSI)<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




