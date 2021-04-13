---
UID: ''
title: InterlockedPushListSList-Funktion
description: Fügt eine einzeln verknüpfte Liste an der Vorderseite einer anderen verknüpften Liste ein.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: InterlockedPushListSListEx
ms.topic: reference
req.header:
- WinBase.h on Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2
- InterlockedAPI.h on Windows 8 and Windows Server 2012
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-interlocked-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-interlocked-l1-1-0.dll
api_name:
- InterlockedPushListSList
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: ccecdae3af5119a86594c31856dac11ecb4507bc
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "104390073"
---
# <a name="interlockedpushlistslist-function"></a>InterlockedPushListSList-Funktion

## <a name="description"></a>BESCHREIBUNG

Fügt eine einzeln verknüpfte Liste an der Vorderseite einer anderen verknüpften Liste ein.
Der Zugriff auf die Listen wird auf einem Multiprozessorsystem synchronisiert.

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a>Parameter

### <a name="listhead-in-out"></a>Lisder AD [in, out]

Ein Zeiger auf eine **SLIST_HEADER** -Struktur, die die Kopfzeile einer einzeln verknüpften Liste darstellt.
Die Liste, die von den Parametern *List* und *listend* angegeben wird, wird am Anfang der Liste eingefügt.

### <a name="list-in-out"></a>List [in, out]

Ein Zeiger auf eine [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) -Struktur, die das erste Element in der Liste darstellt, das eingefügt werden soll.

### <a name="listend-in-out"></a>Listend [in, out]

Ein Zeiger auf eine [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) -Struktur, die das letzte Element in der Liste darstellt, das eingefügt werden soll.

### <a name="count-in"></a>Count [in]

Die Anzahl der Elemente in der Liste, die eingefügt werden soll.

## <a name="returns"></a>Gibt zurück

Der Rückgabewert ist das vorherige erste Element in der Liste, die durch den *listead* -Parameter angegeben wird.
Wenn die Liste zuvor leer war, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Alle Listenelemente müssen an einer **MEMORY_ALLOCATION_ALIGNMENT** Grenze ausgerichtet werden. Andernfalls verhält sich diese Funktion unvorhersehbar.
Siehe **_aligned_malloc**.

**Windows 8 und Windows Server 2012:**  Diese Funktion wurde durch [interlockedpushlistslistex](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)ersetzt.
Bei der Kompilierung mit **NTDDI_VERSION** auf **NTDDI_WIN8** oder höher festgelegt, werden Aufrufe von **interlockedpushlistslist** stattdessen an **interlockedpushlistslistex** weitergeleitet.

## <a name="see-also"></a>Siehe auch

[Miteinander verknüpfte, einzeln verknüpfte Listen](/windows/desktop/Sync/interlocked-singly-linked-lists)

[Interlockedpopentryslist](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[Interlockedpushentryslist](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[Interlockedpushlistslistex](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[Interlockedflushslist](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry)

[Verwenden von einzeln verknüpften Listen](/windows/desktop/Sync/using-singly-linked-lists)
