---
description: Die selectnppblobfromtable-Funktion wählt eine NIC aus einer angegebenen NPP-BLOB-Tabelle aus.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: Selectnppblobfromtable-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d8f504d76d43b8a398947f435f7bd488678ea394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214758"
---
# <a name="selectnppblobfromtable-function"></a>Selectnppblobfromtable-Funktion

Die **selectnppblobfromtable** -Funktion wählt eine NIC aus einer angegebenen NPP-BLOB-Tabelle aus.

## <a name="syntax"></a>Syntax


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle für das Fenster, das das Dialogfeld " **Netzwerk auswählen** " anzeigt.

</dd> <dt>

*pblobtable* \[ in\]
</dt> <dd>

Ein Zeiger auf die angegebene BLOB-Tabelle. Netzwerkmonitor verwendet diese Tabelle, um das Dialogfeld **Netzwerk auswählen** aufzufüllen.

</dd> <dt>

*hblob* \[ vorgenommen\]
</dt> <dd>

Handle für das BLOB, das die ausgewählte NIC darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wurde und der Benutzer eine NIC auswählt, ist der Rückgabewert nmerr \_ Success; das BLOB, auf das *hblob* verweist, wird ausgefüllt.

Wenn der Benutzer keine NIC auswählt, wird der Rückgabewert nmerr \_ No \_ NPP \_ ausgewählt.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein weiterer nmerr-Wert.

## <a name="remarks"></a>Bemerkungen

Wenn Sie aufgerufen wird, zeigt Netzwerkmonitor das Dialogfeld **Netzwerk auswählen** an, mit dem Sie eine NIC auswählen können. Das NPP-BLOB, das die ausgewählte NIC darstellt, kehrt zur aufrufenden Anwendung zurück.

Weitere Informationen zu den verschiedenen Möglichkeiten, NICs auszuwählen, finden Sie unter [Auswählen einer Netzwerkschnittstellenkarte](selecting-a-network-interface-card.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Getnppblobfromui](getnppblobfromui.md)
</dt> <dt>

[Getnppblobtable](getnppblobtable.md)
</dt> <dt>

[Spezielle BLOB-Einträge](special-blob-entries.md)
</dt> </dl>

 

 




